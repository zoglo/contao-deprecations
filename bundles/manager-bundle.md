# contao/manager-bundle deprecations (4.13)

## Bundles
- [calendar-bundle](calendar-bundle#deprecations)
- [core-bundle](core-bundle#deprecations)
- [comments-bundle](comments-bundle#deprecations)
- [faq-bundle](faq-bundle#deprecations)
- [installation-bundle](installation-bundle#deprecations)
- [manager-bundle](manager-bundle#deprecations)
- [news-bundle](news-bundle#deprecations)
- [newsletter-bundle](newsletter-bundle#deprecations)

____

## Deprecations

### configurations

```yml
#services.yml
services:
    # Backwards compatibility
    contao_manager.routing_loader:
        alias: contao_manager.routing.route_loader
        public: true
        deprecated:
            package: contao/manager-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao_manager.routing.route_loader" instead.
```

### php-docs / annotations

```php
namespace Contao\ManagerBundle\Composer;

/**
 * @deprecated Deprecated since Contao 4.11, to be removed in Contao 5.0; use
 *             the "contao-setup" binary instead.
 */
class ScriptHandler
{
/**
     * Runs all Composer tasks to initialize a Contao Managed Edition.
     */
    public static function initializeApplication(Event $event): void
    {
        trigger_deprecation('contao/manager-bundle', '4.11', 'Using ScriptHandler::initializeApplication() has been deprecated and will no longer work in Contao 5.0. Use the "contao-setup" binary instead.');
        //...
    }

    public static function purgeCacheFolder(): void
    {
        trigger_deprecation('contao/manager-bundle', '4.11', 'Using ScriptHandler::purgeCacheFolder() has been deprecated and will no longer work in Contao 5.0.');

        $filesystem = new Filesystem();
        $filesystem->removeDirectory(Path::join(getcwd(), 'var/cache/prod'));
    }

    /**
     * Adds the app directory if it does not exist.
     */
    public static function addAppDirectory(): void
    {
        trigger_deprecation('contao/manager-bundle', '4.11', 'Using ScriptHandler::addAppDirectory() has been deprecated and will no longer work in Contao 5.0.');

        $filesystem = new Filesystem();
        $filesystem->ensureDirectoryExists(Path::join(getcwd(), 'app'));
    }
```

```php
namespace Contao\ManagerBundle\HttpKernel;

class ContaoKernel extends Kernel implements HttpCacheProvider
{
    /**
     * @deprecated since Symfony 4.2, use getProjectDir() instead
     */
    public function getRootDir(): string
    {
        return Path::join($this->getProjectDir(), 'app');
    }
```

```php
namespace Contao\ManagerBundle\ContaoManager;

class Plugin implements BundlePluginInterface, ConfigPluginInterface, RoutingPluginInterface, ExtensionPluginInterface, DependentPluginInterface, ApiPluginInterface
{
    public function getExtensionConfig($extensionName, array $extensionConfigs, PluginContainerBuilder $container): array
    {
        switch ($extensionName) {
            case 'contao':
                return $this->handlePrependLocale($extensionConfigs, $container);

            case 'framework':
                $extensionConfigs = $this->checkMailerTransport($extensionConfigs, $container);
                $extensionConfigs = $this->addDefaultMailer($extensionConfigs, $container);

                if (!isset($_SERVER['APP_SECRET'])) {
                    $container->setParameter('env(APP_SECRET)', $container->getParameter('secret'));
                }

                if (!isset($_SERVER['MAILER_DSN'])) {
                    if (isset($_SERVER['MAILER_URL'])) {
                        trigger_deprecation('contao/manager-bundle', '4.13', 'Using the "MAILER_URL" environment variable has been deprecated and will no longer work in Contao 5.0. Use the "MAILER_DSN" environment variable instead.');
                        $container->setParameter('env(MAILER_DSN)', $this->getMailerDsnFromMailerUrl($_SERVER['MAILER_URL']));
                    } else {
                        $container->setParameter('env(MAILER_DSN)', $this->getMailerDsn($container));
                    }
                }

                return $extensionConfigs;
        }
        //...
    }

    private function handlePrependLocale(array $extensionConfigs, ContainerBuilder $container): array
    {
        //...
        trigger_deprecation('contao/manager-bundle', '4.6', 'Defining the "prepend_locale" parameter in the parameters.yml file has been deprecated and will no longer work in Contao 5.0. Define the "contao.prepend_locale" parameter in the config.yml file instead.');

        $extensionConfigs[] = [
            'prepend_locale' => '%prepend_locale%',
        ];

        return $extensionConfigs;
    }
```

```php
namespace Contao\ManagerBundle\HttpKernel;

class ContaoCache extends HttpCache implements CacheInvalidation
{
    private function readEnvCsv(string $key, string $oldName = ''): array
    {
        if ('' !== $oldName && isset($_SERVER[$oldName])) {
            trigger_deprecation('contao/manager-bundle', '4.10', sprintf('Using the "%s" environment variable has been deprecated. Use "%s" instead.', $oldName, $key));

            $key = $oldName;
        }

        return array_filter(explode(',', $_SERVER[$key] ?? ''));
    }
```

```php
namespace Contao\ManagerBundle\HttpKernel;

class ContaoKernel extends Kernel implements HttpCacheProvider
{
    private function getConfigFile(string $file, ContainerBuilder $container): ?string
    {
        //...
        // Fallback to the legacy config file (see #566)
        foreach (['.yaml', '.yml'] as $ext) {
            $path = Path::join($projectDir, 'app/config', $file.$ext);

            // Only trigger deprecation if no file exists in the root config folder
            if ($container->fileExists($path) && [] === $exists) {
                trigger_deprecation('contao/manager-bundle', '4.9', sprintf('Storing the "%s" file in the "app/config" folder has been deprecated and will no longer work in Contao 5.0. Move it to the "config" folder instead.', $file.$ext));
                $exists[] = $path;
            }
        }

        return $exists[0] ?? null;
    }
```

```php
namespace Contao\ManagerBundle\Routing;

class RouteLoader implements RouteLoaderInterface
{
    private function getConfigFile(): ?string
    {
        foreach (['routes.yaml', 'routes.yml', 'routing.yaml', 'routing.yml'] as $file) {
            $path = Path::join($this->projectDir, 'config', $file);

            if (file_exists($path)) {
                if ('routing' === Path::getFilenameWithoutExtension($file)) {
                    trigger_deprecation('contao/manager-bundle', '4.9', sprintf('Using a "%s" file has been deprecated and will no longer work in Contao 5.0. Rename it to "routes.yaml" instead.', $file));
                }

                return $path;
            }
        }

        // Fallback to the legacy config file (see #566)
        foreach (['routes.yaml', 'routes.yml', 'routing.yaml', 'routing.yml'] as $file) {
            $path = Path::join($this->projectDir, 'app/config', $file);

            if (file_exists($path)) {
                trigger_deprecation('contao/manager-bundle', '4.9', sprintf('Storing the "%s" file in the "app/config" folder has been deprecated and will no longer work in Contao 5.0. Move it to the "config" folder instead.', $file));

                return $path;
            }
        }

        return null;
    }
```
