# contao/core-bundle deprecations (4.13)

## Bundles
- [calendar-bundle](calendar-bundle.md#deprecations)
- [core-bundle](core-bundle.md#deprecations)
- [comments-bundle](comments-bundle.md#deprecations)
- [faq-bundle](faq-bundle.md#deprecations)
- [installation-bundle](installation-bundle.md#deprecations)
- [manager-bundle](manager-bundle.md#deprecations)
- [news-bundle](news-bundle.md#deprecations)
- [newsletter-bundle](newsletter-bundle.md#deprecations)

____

## Deprecations

### configurations

```yml
#commands.yml
services:
    contao.command.version:
        class: Contao\CoreBundle\Command\VersionCommand
        deprecated:
            package: contao/core-bundle
            version: 4.4
            message: Using the "%service_id%" service ID has been deprecated and will no longer work in Contao 5.0.
```

```yml
#controller.yml
services:
    # Backwards compatibility
    contao.controller.backend_csv_import:
        alias: Contao\CoreBundle\Controller\BackendCsvImportController
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.9
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "Contao\CoreBundle\Controller\BackendCsvImportController" instead.

    contao.controller.images:
        alias: Contao\CoreBundle\Controller\ImagesController
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.9
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "Contao\CoreBundle\Controller\ImagesController" instead.

    contao.controller.insert_tags:
        alias: Contao\CoreBundle\Controller\InsertTagsController
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.9
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "Contao\CoreBundle\Controller\InsertTagsController" instead.
```

```yml
#listener.yml
services:
    # Backwards compatibility
    Contao\CoreBundle\EventListener\DataContainer\ContentCompositionListener:
        alias: contao.listener.data_container.content_composition
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.listener.data_container.content_composition" instead.

    Contao\CoreBundle\EventListener\DataContainer\PageTypeOptionsListener:
        alias: contao.listener.data_container.page_type_options
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.listener.data_container.page_type_options" instead.

    Contao\CoreBundle\EventListener\DataContainer\PageUrlListener:
        alias: contao.listener.data_container.page_url
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.listener.data_container.page_url" instead.
```

```yml
#migrations.yml
services:
    # Backwards compatibility
    Contao\CoreBundle\Migration\MigrationCollection:
        alias: contao.migration.collection
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.migration.collection" instead.
```

```yml
#services.yml
services:
    # Backwards compatibility
    contao.cache.clear_internal:
        alias: contao.cache.clearer
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.cache.clearer" instead.

    contao.cache.warm_internal:
        alias: contao.cache.warmer
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.cache.warmer" instead.

    contao.crawl.escargot_factory:
        alias: contao.crawl.escargot.factory
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.crawl.escargot.factory" instead.

    contao.image.image_factory:
        alias: contao.image.factory
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.image.factory" instead.

    contao.image.image_sizes:
        alias: contao.image.sizes
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.image.sizes" instead.

    contao.image.resizer:
        alias: contao.image.legacy_resizer
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.image.legacy_resizer" instead.

    contao.opt-in:
        alias: contao.opt_in
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.opt_in" instead.

    Contao\CoreBundle\Cron\Cron:
        alias: contao.cron
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.cron" instead.

    Contao\CoreBundle\Framework\ContaoFrameworkInterface:
        alias: contao.framework
        deprecated:
            package: contao/core-bundle
            version: 4.9
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.framework" instead.

    Contao\CoreBundle\Image\Studio\FigureRenderer:
        alias: contao.image.studio.figure_renderer
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.image.studio.figure_renderer" instead.

    Contao\CoreBundle\Routing\ResponseContext\CoreResponseContextFactory:
        alias: contao.routing.response_context_factory
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.routing.response_context_factory" instead.

    Contao\CoreBundle\Security\TwoFactor\BackupCodeManager:
        alias: contao.security.two_factor.backup_code_manager
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.security.two_factor.backup_code_manager" instead.

    Contao\CoreBundle\Twig\Extension\ContaoExtension:
        alias: contao.twig.extension
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.twig.extension" instead.

    Contao\CoreBundle\Twig\Loader\ThemeNamespace:
        alias: contao.twig.loader.theme_namespace
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.twig.loader.theme_namespace" instead.

    Contao\CoreBundle\Twig\Loader\TemplateLocator:
        alias: contao.twig.loader.template_locator
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.twig.loader.template_locator" instead.

    Contao\CoreBundle\Twig\Loader\ContaoFilesystemLoaderWarmer:
        alias: contao.twig.filesystem_loader_warmer
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.twig.filesystem_loader_warmer" instead.

    Contao\CoreBundle\Util\SimpleTokenExpressionLanguage:
        alias: contao.string.simple_token_expression_language
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.string.simple_token_expression_language" instead.

    Contao\CoreBundle\Util\SimpleTokenParser:
        alias: contao.string.simple_token_parser
        public: true
        deprecated:
            package: contao/core-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao.string.simple_token_parser" instead.

```

### php-docs / annotations

```php
namespace Contao\CoreBundle;

/**
 * @deprecated Deprecated since Contao 4.1, to be removed in Contao 5.0; use the
 *             Contao\CoreBundle\Framework\ContaoFrameworkInterface interface instead
 */
interface ContaoFrameworkInterface
```

```php
namespace Contao\CoreBundle\Command;

/**
 * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.0; use
 *             the Symfony Lock component instead
 */
abstract class AbstractLockedCommand extends Command implements ContainerAwareInterface
{
```

```php
namespace Contao\CoreBundle\Command;

/**
 * @internal
 *
 * @deprecated Deprecated since Contao 4.4, to be removed in Contao 5.0; use
 *             "composer show | grep contao/core-bundle | awk '{ print $2 }'" instead
 */
class VersionCommand extends Command
```

```php
namespace Contao\CoreBundle\Controller;

/**
 * @Route(path="%contao.backend.route_prefix%", defaults={"_scope" = "backend"})
 *
 * @internal
 */
class BackendController extends AbstractController
{
    /**
     * @Route("/file", name="contao_backend_file", defaults={"_store_referrer" = false})
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use the picker instead.
     */
    public function fileAction(): Response
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Calling "%s()" has been deprecated and will no longer work in Contao 5.0. Use the picker instead.', __METHOD__);

        $this->initializeContaoFramework();

        $controller = new BackendFile();

        return $controller->run();
    }

    /**
     * @Route("/page", name="contao_backend_page", defaults={"_store_referrer" = false})
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use the picker instead.
     */
    public function pageAction(): Response
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Calling "%s::%s()" has been deprecated and will no longer work in Contao 5.0. Use the picker instead.', __CLASS__, __METHOD__);

        $this->initializeContaoFramework();

        $controller = new BackendPage();

        return $controller->run();
    }
```

```php
namespace Contao\CoreBundle\Controller;

/**
 * Custom controller to support legacy entry points.
 *
 * @internal
 *
 * @deprecated Deprecated in Contao 4.0, to be removed in Contao 5.0
 *
 * @Route("/_contao/initialize", name="contao_initialize")
 */
class InitializeController
{
```

```php
namespace Contao\CoreBundle\DependencyInjection\Compiler;

/**
 * Adds the composer packages and version numbers to the container.
 *
 * @internal
 *
 * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0; use
 *             the Composer\InstalledVersions class instead
 */
class AddPackagesPass implements CompilerPassInterface
```

```php
namespace Contao\CoreBundle\Doctrine\Schema;

class DcaSchemaProvider
{
    /**
     * @deprecated Deprecated since Contao 4.11, to be removed in Contao 5.0;
     *             use the Contao\CoreBundle\Doctrine\Schema\SchemaProvider
     *             class instead.
     */
    public function createSchema(): Schema
    {
        trigger_deprecation('contao/core-bundle', '4.11', 'Using the DcaSchemaProvider class to create the schema has been deprecated and will no longer work in Contao 5.0. Use the Contao\CoreBundle\Doctrine\Schema\SchemaProvider\SchemaProvider class instead.');

        return $this->schemaProvider->createSchema();
    }
```

```php
namespace Contao\CoreBundle\EventListener;

/**
 * @internal
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0
 */
class InitializeControllerListener
{
```

```php
namespace Contao\CoreBundle\EventListener;

/**
 * @internal
 *
 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
 */
class LegacyLoginConstantsListener
{
```

```php
namespace Contao\CoreBundle\EventListener;

trigger_deprecation('contao/core-bundle', '4.3', 'Using the "Contao\CoreBundle\EventListener\UserAwareTrait" trait has been deprecated and will no longer work in Contao 5.0.');

/**
 * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0
 */
trait UserAwareTrait
{
```

```php
namespace Contao\CoreBundle\EventListener\HttpCache;

/**
 * @internal
 */
class StripCookiesSubscriber implements EventSubscriberInterface
{
    /**
     * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0; use the
     *             getAllowList() method instead
     */
    public function getWhitelist(): array
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using the "getWhitelist()" method has been deprecated and will no longer work in Contao 5.0. Use the "getAllowList()" method instead.');

        return $this->getAllowList();
    }
```

```php
namespace Contao\CoreBundle\Exception;

trigger_deprecation('contao/core-bundle', '4.7', 'Using the "Contao\CoreBundle\Exception\PaletteNotFoundException" class has been deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\DataContainer\PaletteNotFoundException" class instead.');

/**
 * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.0; use the
 *             Contao\CoreBundle\DataContainer\PaletteNotFoundException instead
 */
class PaletteNotFoundException extends \InvalidArgumentException
{
```

```php
namespace Contao\CoreBundle\Exception;

trigger_deprecation('contao/core-bundle', '4.7', 'Using the "Contao\CoreBundle\Exception\PalettePositionException" class has been deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\DataContainer\PalettePositionException" class instead.');

/**
 * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.0; use the
 *             Contao\CoreBundle\DataContainer\PalettePositionException instead
 */
class PalettePositionException extends \InvalidArgumentException
{

```

```php
namespace Contao\CoreBundle\Filesystem\Dbafs;

class Dbafs implements DbafsInterface, ResetInterface
{
    /**
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     */
    public function setMaxFileSize(int $bytes): void
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Setting a maximum file size has no effect anymore. The "%s()" method will be removed in Contao 5.', __METHOD__);
    }
```

```php
namespace Contao\CoreBundle\Framework;

/**
 * @internal Do not use this class in your code; use the "contao.framework" service instead
 */
class ContaoFramework implements ContaoFrameworkInterface, ContainerAwareInterface, ResetInterface
{
    /**
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function setLoginConstants(): void
    {
        // Check if the constants have already been defined (see #5137)
        if (\defined('BE_USER_LOGGED_IN') || \defined('FE_USER_LOGGED_IN')) {
            return;
        }

        // If the framework has not been initialized yet, set the login constants on init (#4968)
        if (!$this->isInitialized()) {
            $this->setLoginConstantsOnInit = true;

            return;
        }

        if ('FE' === $this->getMode()) {
            \define('BE_USER_LOGGED_IN', $this->tokenChecker->isPreviewMode());
            \define('FE_USER_LOGGED_IN', $this->tokenChecker->hasFrontendUser());
        } else {
            \define('BE_USER_LOGGED_IN', false);
            \define('FE_USER_LOGGED_IN', false);
        }
    }

    /**
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0
     */
    private function setConstants(): void
    {
        if (!\defined('TL_MODE')) {
            \define('TL_MODE', $this->getMode());
        }

        \define('TL_START', microtime(true));
        \define('TL_ROOT', $this->projectDir);
        \define('TL_REFERER_ID', $this->getRefererId());

        if (!\defined('TL_SCRIPT')) {
            \define('TL_SCRIPT', $this->getRoute());
        }

        // Define the login status constants (see #4099, #5279)
        if ($this->setLoginConstantsOnInit || null === $this->requestStack->getCurrentRequest()) {
            $this->setLoginConstants();
        }

        // Define the relative path to the installation (see #5339)
        \define('TL_PATH', $this->getPath());
    }
```

```php
namespace Contao\CoreBundle\Framework;

/**
 * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.0; use the
 *             Contao\CoreBundle\Framework\ContaoFramework class instead
 */
interface ContaoFrameworkInterface extends \Contao\CoreBundle\ContaoFrameworkInterface
{
```

```php
namespace Contao\CoreBundle\Framework;

trait FrameworkAwareTrait
{
    /**
     * @throws \LogicException
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0
     */
    public function getFramework(): ContaoFramework
    {
```

```php
namespace Contao\CoreBundle\Framework;

trigger_deprecation('contao/core-bundle', '4.4', 'Using the "Contao\CoreBundle\Framework\ScopeAwareTrait" trait has been deprecated and will no longer work in Contao 5.0. Use the "contao.routing.scope_matcher" service instead.');

/**
 * @deprecated Deprecated since Contao 4.4, to be removed in Contao 5.0; use
 *             the contao.routing.scope_matcher service instead
 */
trait ScopeAwareTrait
{
```

```php
namespace Contao\CoreBundle\Picker;

abstract class AbstractPickerProvider implements PickerProviderInterface
{
    /**
     * @deprecated Deprecated since Contao 4.8, to be removed in Contao 5.0;
     *             use Symfony security instead
     */
    public function setTokenStorage(TokenStorageInterface $tokenStorage): void
    {
        trigger_deprecation('contao/core-bundle', '4.8', 'Using "Contao\CoreBundle\Picker\AbstractPickerProvider::setTokenStorage()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        $this->tokenStorage = $tokenStorage;
    }

    public function isCurrent(PickerConfig $config)/*: bool*/
    {
        return $config->getCurrent() === $this->getName();
    }

    /**
     * Returns the back end user object.
     *
     * @throws \RuntimeException
     *
     * @deprecated Deprecated since Contao 4.8, to be removed in Contao 5.0;
     *             use Symfony security instead
     */
    protected function getUser(): BackendUser
    {
        trigger_deprecation('contao/core-bundle', '4.8', 'Using "Contao\CoreBundle\Picker\AbstractPickerProvider::getUser()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        if (null === $this->tokenStorage) {
            throw new \RuntimeException('No token storage provided');
        }

        $token = $this->tokenStorage->getToken();

        if (null === $token) {
            throw new \RuntimeException('No token provided');
        }

        $user = $token->getUser();

        if (!$user instanceof BackendUser) {
            throw new \RuntimeException('The token does not contain a back end user object');
        }

        return $user;
    }
```

```php
namespace Contao;

/**
 * Provide methods to manage back end controllers.
 *
 * @property Ajax $objAjax
 */
abstract class Backend extends Controller
{
    /**
     * Return a list of TinyMCE templates as JSON string
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0
     */
    public static function getTinyTemplates()
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "Backend::getTinyTemplates()" has been deprecated and will no longer work in Contao 5.0.');

        $strDir = System::getContainer()->getParameter('contao.upload_path') . '/tiny_templates';
        $projectDir = System::getContainer()->getParameter('kernel.project_dir');

        if (!is_dir($projectDir . '/' . $strDir))
        {
            return '';
        }

        $arrFiles = array();
        $arrTemplates = Folder::scan($projectDir . '/' . $strDir);

        foreach ($arrTemplates as $strFile)
        {
            if (strncmp('.', $strFile, 1) !== 0 && is_file($projectDir . '/' . $strDir . '/' . $strFile))
            {
                $arrFiles[] = '{ title: "' . $strFile . '", url: "' . $strDir . '/' . $strFile . '" }';
            }
        }

        return implode(",\n", $arrFiles) . "\n";
    }

    /**
     * Get all searchable pages and return them as array
     *
     * @param integer $pid
     * @param string  $domain
     * @param boolean $blnIsXmlSitemap
     *
     * @return array
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0
     */
    public static function findSearchablePages($pid=0, $domain='', $blnIsXmlSitemap=false)
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using "Backend::findSearchablePages()" has been deprecated and will no longer work in Contao 5.0.');

        // Since the publication status of a page is not inherited by its child
        // pages, we have to use findByPid() instead of findPublishedByPid() and
        // filter out unpublished pages in the foreach loop (see #2217)
        $objPages = PageModel::findByPid($pid, array('order'=>'sorting'));

        if ($objPages === null)
        {
            return array();
        }

        $arrPages = array();
        $user = null;

        if (Config::get('indexProtected') && System::getContainer()->get('contao.security.token_checker')->hasFrontendUser())
        {
            $user = FrontendUser::getInstance();
        }

        // Recursively walk through all subpages
        foreach ($objPages as $objPage)
        {
            $objPage->loadDetails();

            // PageModel->groups is an array after calling loadDetails()
            // Cannot use security voters across firewall context (backend to frontend)
            $indexProtected = (!$user && \in_array(-1, $objPage->groups)) || ($user && $user->isMemberOf($objPage->groups));
            $isPublished = ($objPage->published && (!$objPage->start || $objPage->start <= time()) && (!$objPage->stop || $objPage->stop > time()));

            // Searchable and not protected
            if ($isPublished && $objPage->type == 'regular' && !$objPage->requireItem && (!$objPage->noSearch || $blnIsXmlSitemap) && (!$blnIsXmlSitemap || $objPage->robots != 'noindex,nofollow') && (!$objPage->protected || $indexProtected))
            {
                $arrPages[] = $objPage->getAbsoluteUrl();

                // Get articles with teaser
                if (($objArticles = ArticleModel::findPublishedWithTeaserByPid($objPage->id, array('ignoreFePreview'=>true))) !== null)
                {
                    foreach ($objArticles as $objArticle)
                    {
                        $arrPages[] = $objPage->getAbsoluteUrl('/articles/' . ($objArticle->alias ?: $objArticle->id));
                    }
                }
            }

            // Get subpages
            if ((!$objPage->protected || $indexProtected) && ($arrSubpages = static::findSearchablePages($objPage->id, $domain, $blnIsXmlSitemap)))
            {
                $arrPages = array_merge($arrPages, $arrSubpages);
            }
        }

        return $arrPages;
    }

    /**
     * Add the file meta information to the request
     *
     * @param string  $strUuid
     * @param string  $strPtable
     * @param integer $intPid
     *
     * @deprecated Deprecated since Contao 4.4, to be removed in Contao 5.0.
     */
    public static function addFileMetaInformationToRequest($strUuid, $strPtable, $intPid)
    {
        trigger_deprecation('contao/core-bundle', '4.4', 'Using "Contao\Backend::addFileMetaInformationToRequest()" has been deprecated and will no longer work in Contao 5.0.');

        $objFile = FilesModel::findByUuid($strUuid);

        if ($objFile === null)
        {
            return;
        }

        $arrMeta = StringUtil::deserialize($objFile->meta);

        if (empty($arrMeta))
        {
            return;
        }

        $objPage = null;

        if ($strPtable == 'tl_article')
        {
            $objPage = PageModel::findOneBy(array('tl_page.id=(SELECT pid FROM tl_article WHERE id=?)'), $intPid);
        }
        elseif (isset($GLOBALS['TL_HOOKS']['addFileMetaInformationToRequest']) && \is_array($GLOBALS['TL_HOOKS']['addFileMetaInformationToRequest']))
        {
            // HOOK: support custom modules
            foreach ($GLOBALS['TL_HOOKS']['addFileMetaInformationToRequest'] as $callback)
            {
                if (($val = System::importStatic($callback[0])->{$callback[1]}($strPtable, $intPid)) !== false)
                {
                    $objPage = $val;
                }
            }

            if ($objPage instanceof Result && $objPage->numRows < 1)
            {
                return;
            }

            if (\is_object($objPage) && !($objPage instanceof PageModel))
            {
                $objPage = PageModel::findByPk($objPage->id);
            }
        }

        if ($objPage === null)
        {
            return;
        }

        $objPage->loadDetails();

        // Convert the language to a locale (see #5678)
        $strLanguage = LocaleUtil::formatAsLocale($objPage->rootLanguage);

        if (isset($arrMeta[$strLanguage]))
        {
            if (!empty($arrMeta[$strLanguage]['title']) && !Input::post('title'))
            {
                Input::setPost('title', $arrMeta[$strLanguage]['title']);
            }

            if (!empty($arrMeta[$strLanguage]['alt']) && !Input::post('alt'))
            {
                Input::setPost('alt', $arrMeta[$strLanguage]['alt']);
            }

            if (!empty($arrMeta[$strLanguage]['caption']) && !Input::post('caption'))
            {
                Input::setPost('caption', $arrMeta[$strLanguage]['caption']);
            }
        }
    }
```

```php
namespace Contao;

class BackendUser extends User
{
    /**
     * Edit page flag
     * @deprecated Deprecated since Contao 4.13. Use Symfony security and ContaoCorePermissions::USER_CAN_EDIT_PAGE.
     */
    const CAN_EDIT_PAGE = 1;

    /**
     * Edit page hierarchy flag
     * @deprecated Deprecated since Contao 4.13. Use Symfony security and ContaoCorePermissions::USER_CAN_EDIT_PAGE_HIERARCHY.
     */
    const CAN_EDIT_PAGE_HIERARCHY = 2;

    /**
     * Delete page flag
     * @deprecated Deprecated since Contao 4.13. Use Symfony security and ContaoCorePermissions::USER_CAN_DELETE_PAGE.
     */
    const CAN_DELETE_PAGE = 3;

    /**
     * Edit articles flag
     * @deprecated Deprecated since Contao 4.13. Use Symfony security and ContaoCorePermissions::USER_CAN_EDIT_ARTICLES.
     */
    const CAN_EDIT_ARTICLES = 4;

    /**
     * Edit article hierarchy flag
     * @deprecated Deprecated since Contao 4.13. Use Symfony security and ContaoCorePermissions::USER_CAN_EDIT_ARTICLE_HIERARCHY.
     */
    const CAN_EDIT_ARTICLE_HIERARCHY = 5;

    /**
     * Delete articles flag
     * @deprecated Deprecated since Contao 4.13. Use Symfony security and ContaoCorePermissions::USER_CAN_DELETE_ARTICLES.
     */
    const CAN_DELETE_ARTICLES = 6;

    /**
     * Symfony Security session key
     * @deprecated Deprecated since Contao 4.8, to be removed in Contao 5.0
     */
    const SECURITY_SESSION_KEY = '_security_contao_backend';

    /**
     * Redirect to the login screen if authentication fails
     *
     * @return boolean True if the user could be authenticated
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    public function authenticate()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\BackendUser::authenticate()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        // Do not redirect if authentication is successful
        if (System::getContainer()->get('contao.security.token_checker')->hasBackendUser())
        {
            return true;
        }

        if (!$request = System::getContainer()->get('request_stack')->getCurrentRequest())
        {
            return false;
        }

        $route = $request->attributes->get('_route');

        if ($route == 'contao_backend_login')
        {
            return false;
        }

        $url = System::getContainer()->get('router')->generate('contao_backend_login', array('redirect' => $request->getUri()), UrlGeneratorInterface::ABSOLUTE_URL);

        throw new RedirectResponseException(System::getContainer()->get('uri_signer')->sign($url));
    }

    /**
     * Try to login the current user
     *
     * @return boolean True if the user could be logged in
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    public function login()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\BackendUser::login()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        return System::getContainer()->get('contao.security.token_checker')->hasBackendUser();
    }

    /**
     * Return true if the current user is allowed to do the current operation on the current page
     *
     * @param integer $int
     * @param array   $row
     *
     * @return boolean
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use the "security.helper" service with the ContaoCorePermissions
     *             constants instead.
     */
    public function isAllowed($int, $row)
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "Contao\BackendUser::isAllowed()" has been deprecated and will no longer work in Contao 5. Use the "security.helper" service with the ContaoCorePermissions constants instead.');

        if ($this->isAdmin)
        {
            return true;
        }

        // Inherit CHMOD settings
        if (!$row['includeChmod'])
        {
            $pid = $row['pid'];

            $row['chmod'] = false;
            $row['cuser'] = false;
            $row['cgroup'] = false;

            $objParentPage = PageModel::findById($pid);

            while ($objParentPage !== null && $row['chmod'] === false && $pid > 0)
            {
                $pid = $objParentPage->pid;

                $row['chmod'] = $objParentPage->includeChmod ? $objParentPage->chmod : false;
                $row['cuser'] = $objParentPage->includeChmod ? $objParentPage->cuser : false;
                $row['cgroup'] = $objParentPage->includeChmod ? $objParentPage->cgroup : false;

                $objParentPage = PageModel::findById($pid);
            }

            // Set default values
            if ($row['chmod'] === false)
            {
                $row['chmod'] = Config::get('defaultChmod');
            }

            if ($row['cuser'] === false)
            {
                $row['cuser'] = (int) Config::get('defaultUser');
            }

            if ($row['cgroup'] === false)
            {
                $row['cgroup'] = (int) Config::get('defaultGroup');
            }
        }

        // Set permissions
        $chmod = StringUtil::deserialize($row['chmod']);
        $chmod = \is_array($chmod) ? $chmod : array($chmod);
        $permission = array('w' . $int);

        if (\in_array($row['cgroup'], $this->groups))
        {
            $permission[] = 'g' . $int;
        }

        if ($row['cuser'] == $this->id)
        {
            $permission[] = 'u' . $int;
        }

        return \count(array_intersect($permission, $chmod)) > 0;
    }

    /**
     * Return true if there is at least one allowed excluded field
     *
     * @param string $table
     *
     * @return boolean
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use the "security.helper" service with the ContaoCorePermissions::USER_CAN_EDIT_FIELDS_OF_TABLE
     *             constant instead.
     */
    public function canEditFieldsOf($table)
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "Contao\BackendUser::canEditFieldsOfTable()" has been deprecated and will no longer work in Contao 5. Use the "security.helper" service with the ContaoCorePermissions::USER_CAN_EDIT_FIELDS_OF_TABLE constant instead.');

        if ($this->isAdmin)
        {
            return true;
        }

        return \count(preg_grep('/^' . preg_quote($table, '/') . '::/', $this->alexf)) > 0;
    }

    /**
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0.
     */
    public function serialize()
    {
        $data = $this->__serialize();
        $data['parent'] = serialize($data['parent']);

        return serialize($data);
    }

    public function __serialize(): array
    {
        return array('admin' => $this->admin, 'amg' => $this->amg, 'parent' => parent::__serialize());
    }

    /**
     * @deprecated Deprecated since Contao 4.9 to be removed in Contao 5.0.
     */
    public function unserialize($data)
    {
        $unserialized = unserialize($data, array('allowed_classes'=>false));

        if (!isset($unserialized['parent']))
        {
            return;
        }

        $unserialized['parent'] = unserialize($unserialized['parent'], array('allowed_classes'=>false));

        $this->__unserialize($unserialized);
    }
```

```php
namespace Contao;

abstract class DataContainer extends Backend
{
    /**
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function addCtableTags($strTable, $intId, &$tags)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Calling "%s()" has been deprecated and will no longer work in Contao 5.0.', __METHOD__);

        $ctables = $GLOBALS['TL_DCA'][$strTable]['config']['ctable'] ?? array();

        if (($GLOBALS['TL_DCA'][$strTable]['list']['sorting']['mode'] ?? null) == 5)
        {
            $ctables[] = $strTable;
        }

        if (!$ctables)
        {
            return;
        }

        foreach ($ctables as $ctable)
        {
            Controller::loadDataContainer($ctable);

            if ($GLOBALS['TL_DCA'][$ctable]['config']['dynamicPtable'] ?? null)
            {
                $objIds = $this->Database->prepare('SELECT id FROM ' . Database::quoteIdentifier($ctable) . ' WHERE pid=? AND ptable=?')
                                         ->execute($intId, $strTable);
            }
            else
            {
                $objIds = $this->Database->prepare('SELECT id FROM ' . Database::quoteIdentifier($ctable) . ' WHERE pid=?')
                                         ->execute($intId);
            }

            if (!$objIds->numRows)
            {
                continue;
            }

            while ($objIds->next())
            {
                $tags[] = 'contao.db.' . $ctable . '.' . $objIds->id;

                $this->addCtableTags($ctable, $objIds->id, $tags);
            }
        }
    }
```

```php
namespace Contao;

/**
 * Provide methods to handle file uploads in the back end.
 */
class FileUpload extends Backend
{
    /**
     * Return the maximum upload file size in bytes
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.6, to be removed in Contao 5.0.
     *             Use FileUpload::getMaxUploadSize() instead.
     */
    protected function getMaximumUploadSize()
    {
        trigger_deprecation('contao/core-bundle', '4.6', 'Using "Contao\FileUpload::getMaximumUploadSize()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\FileUpload::getMaxUploadSize()" instead.');

        return static::getMaxUploadSize();
    }
```

```php
namespace Contao;

abstract class Frontend extends Controller
{
    /**
     * Split the current request into fragments, strip the URL suffix, recreate the $_GET array and return the page ID
     *
     * @return mixed
     *
     * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.0.
     *             Use the Symfony routing instead.
     */
    public static function getPageIdFromUrl()
    {
        trigger_deprecation('contao/core-bundle', '4.7', 'Using "Contao\Frontend::getPageIdFromUrl()" has been deprecated and will no longer work in Contao 5.0. Use the Symfony routing instead.');

        if (!System::getContainer()->getParameter('contao.legacy_routing'))
        {
            throw new LegacyRoutingException('Frontend::getPageIdFromUrl() requires legacy routing. Configure "prepend_locale" or "url_suffix" in your app configuration (e.g. config.yml).');
        }

        $strRequest = Environment::get('relativeRequest');

        if (!$strRequest)
        {
            return null;
        }

        // Get the request without the query string
        list($strRequest) = explode('?', $strRequest, 2);

        // URL decode here (see #6232)
        $strRequest = rawurldecode($strRequest);

        // The request string must not contain "auto_item" (see #4012)
        if (strpos($strRequest, '/auto_item/') !== false)
        {
            return false;
        }

        // Extract the language
        if (Config::get('addLanguageToUrl'))
        {
            $arrMatches = array();

            // Use the matches instead of substr() (thanks to Mario Müller)
            if (preg_match('@^([a-z]{2}(-[A-Z]{2})?)/(.*)$@', $strRequest, $arrMatches))
            {
                Input::setGet('language', $arrMatches[1]);

                // Trigger the root page if only the language was given
                if (!$arrMatches[3])
                {
                    return null;
                }

                $strRequest = $arrMatches[3];
            }
            else
            {
                return false; // Language not provided
            }
        }

        // Remove the URL suffix if not just a language root (e.g. en/) is requested
        if ($strRequest && (!Config::get('addLanguageToUrl') || !preg_match('@^[a-z]{2}(-[A-Z]{2})?/$@', $strRequest)))
        {
            $intSuffixLength = \strlen(Config::get('urlSuffix'));

            // Return false if the URL suffix does not match (see #2864)
            if ($intSuffixLength > 0)
            {
                if (substr($strRequest, -$intSuffixLength) != Config::get('urlSuffix'))
                {
                    return false;
                }

                $strRequest = substr($strRequest, 0, -$intSuffixLength);
            }
        }

        $arrFragments = null;

        // Use folder-style URLs
        if (strpos($strRequest, '/') !== false)
        {
            $strAlias = $strRequest;
            $arrOptions = array($strAlias);

            // Compile all possible aliases by applying dirname() to the request (e.g. news/archive/item, news/archive, news)
            while ($strAlias != '/' && strpos($strAlias, '/') !== false)
            {
                $strAlias = \dirname($strAlias);
                $arrOptions[] = $strAlias;
            }

            /** @var ContaoFramework $framework */
            $framework = System::getContainer()->get('contao.framework');
            $objPageModel = $framework->getAdapter(PageModel::class);

            // Check if there are pages with a matching alias
            $objPages = $objPageModel->findByAliases($arrOptions);

            if ($objPages !== null)
            {
                $arrPages = array();

                // Order by domain and language
                while ($objPages->next())
                {
                    /** @var PageModel $objModel */
                    $objModel = $objPages->current();
                    $objPage  = $objModel->loadDetails();

                    $domain = $objPage->domain ?: '*';
                    $arrPages[$domain][$objPage->rootLanguage][] = $objPage;

                    // Also store the fallback language
                    if ($objPage->rootIsFallback)
                    {
                        $arrPages[$domain]['*'][] = $objPage;
                    }
                }

                $arrAliases = array();
                $strHost = Environment::get('host');

                // Look for a root page whose domain name matches the host name
                $arrLangs = $arrPages[$strHost] ?? $arrPages['*'] ?? array();

                // Use the first result (see #4872)
                if (!Config::get('addLanguageToUrl'))
                {
                    $arrAliases = current($arrLangs);
                }
                // Try to find a page matching the language parameter
                elseif (($lang = Input::get('language')) && isset($arrLangs[$lang]))
                {
                    $arrAliases = $arrLangs[$lang];
                }

                // Return if there are no matches
                if (empty($arrAliases))
                {
                    return false;
                }

                $objPage = $arrAliases[0];

                // The request consists of the alias only
                if ($strRequest == $objPage->alias)
                {
                    $arrFragments = array($strRequest);
                }
                // Remove the alias from the request string, explode it and then re-insert the alias at the beginning
                else
                {
                    $arrFragments = explode('/', substr($strRequest, \strlen($objPage->alias) + 1));
                    array_unshift($arrFragments, $objPage->alias);
                }
            }
        }

        // If folderUrl is deactivated or did not find a matching page
        if ($arrFragments === null)
        {
            if ($strRequest == '/')
            {
                return false;
            }

            $arrFragments = explode('/', $strRequest);
        }

        // Add the second fragment as auto_item if the number of fragments is even
        if (\count($arrFragments) % 2 == 0)
        {
            if (!Config::get('useAutoItem'))
            {
                return false; // see #264
            }

            ArrayUtil::arrayInsert($arrFragments, 1, array('auto_item'));
        }

        // HOOK: add custom logic
        if (isset($GLOBALS['TL_HOOKS']['getPageIdFromUrl']) && \is_array($GLOBALS['TL_HOOKS']['getPageIdFromUrl']))
        {
            foreach ($GLOBALS['TL_HOOKS']['getPageIdFromUrl'] as $callback)
            {
                $arrFragments = static::importStatic($callback[0])->{$callback[1]}($arrFragments);
            }
        }

        // Return if the alias is empty (see #4702 and #4972)
        if (!$arrFragments[0] && \count($arrFragments) > 1)
        {
            return false;
        }

        // Add the fragments to the $_GET array
        for ($i=1, $c=\count($arrFragments); $i<$c; $i+=2)
        {
            // Return false if the key is empty (see #4702 and #263)
            if (!$arrFragments[$i])
            {
                return false;
            }

            // Return false if there is a duplicate parameter (duplicate content) (see #4277)
            if (isset($_GET[$arrFragments[$i]]))
            {
                return false;
            }

            // Return false if the request contains an auto_item keyword (duplicate content) (see #4012)
            if (Config::get('useAutoItem') && \in_array($arrFragments[$i], $GLOBALS['TL_AUTO_ITEM']))
            {
                return false;
            }

            Input::setGet($arrFragments[$i], $arrFragments[$i+1], true);
        }

        return $arrFragments[0] ?: null;
    }

    /**
     * Return the root page ID
     *
     * @return integer
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Frontend::getRootPageFromUrl()->id instead.
     */
    public static function getRootIdFromUrl()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Frontend::getRootIdFromUrl()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Frontend::getRootPageFromUrl()->id" instead.');

        return static::getRootPageFromUrl()->id;
    }

    /**
     * Check whether a back end or front end user is logged in
     *
     * @param string $strCookie
     *
     * @return boolean
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    protected function getLoginStatus($strCookie)
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\Frontend::getLoginStatus()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        $objTokenChecker = System::getContainer()->get('contao.security.token_checker');

        if ($strCookie == 'BE_USER_AUTH' && $objTokenChecker->hasBackendUser())
        {
            // Always return false if we are not in preview mode (show hidden elements)
            if (TL_MODE == 'FE' && !$objTokenChecker->isPreviewMode())
            {
                return false;
            }

            return true;
        }

        if ($strCookie == 'FE_USER_AUTH' && $objTokenChecker->hasFrontendUser())
        {
            return true;
        }

        return false;
    }

    /**
     * Prepare a text to be used in the meta description tag
     *
     * @param string $strText
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0;
     *             use the Contao\CoreBundle\String\HtmlDecoder service instead
     */
    protected function prepareMetaDescription($strText)
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using "Contao\Frontend::prepareMetaDescription()" has been deprecated and will no longer work Contao 5.0. Use the "Contao\CoreBundle\String\HtmlDecoder" service instead.');

        $strText = System::getContainer()->get('contao.insert_tag.parser')->replaceInline((string) $strText);
        $strText = strip_tags($strText);
        $strText = str_replace("\n", ' ', $strText);
        $strText = StringUtil::substr($strText, 320);

        return trim($strText);
    }

    /**
     * Return the cron timeout in seconds
     *
     * @return integer
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0.
     */
    public static function getCronTimeout()
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Calling "%s()" has been deprecated and will no longer work in Contao 5.0.', __METHOD__);

        if (!empty($GLOBALS['TL_CRON']['minutely']))
        {
            return 60;
        }

        if (!empty($GLOBALS['TL_CRON']['hourly']))
        {
            return 3600;
        }

        return 86400; // daily
    }

    /**
     * Index a page if applicable
     *
     * @param Response $response
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0.
     *             Use the "contao.search.indexer" service instead.
     */
    public static function indexPageIfApplicable(Response $response)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Using "Contao\Frontend::indexPageIfApplicable()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.search.indexer" service instead.');

        $searchIndexer = System::getContainer()->get('contao.search.indexer');

        // The search indexer is disabled
        if ($searchIndexer === null)
        {
            return;
        }

        $request = System::getContainer()->get('request_stack')->getCurrentRequest();

        if ($request === null)
        {
            throw new \RuntimeException('The request stack did not contain a request');
        }

        $document = Document::createFromRequestResponse($request, $response);

        $searchIndexer->index($document);
    }

    /**
     * Check whether there is a cached version of the page and return a response object
     *
     * @return Response|null
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
     *             Use proper response caching headers instead.
     */
    public static function getResponseFromCache()
    {
        trigger_deprecation('contao/core-bundle', '4.3', 'Using "Contao\Frontend::getResponseFromCache()" has been deprecated and will no longer work in Contao 5.0. Use proper response caching headers instead.');

        return null;
    }
```

```php
namespace Contao;

class FrontendTemplate extends Template
{
    /**
     * Send the response to the client
     *
     * @param bool $blnCheckRequest If true, check for unused $_GET parameters
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use FrontendTemplate::getResponse() instead.
     */
    public function output($blnCheckRequest=false)
    {
        $this->blnCheckRequest = $blnCheckRequest;

        parent::output();
    }
```

```php
namespace Contao;

trait FrontendTemplateTrait
{
    /**
     * Add the template output to the cache and add the cache headers
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
     *             Use proper response caching headers instead.
     */
    protected function addToCache()
    {
        trigger_deprecation('contao/core-bundle', '4.3', 'Using "Contao\FrontendTemplate::addToCache()" has been deprecated and will no longer work in Contao 5.0. Use proper response caching headers instead.');
    }

    /**
     * Add the template output to the search index
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the kernel.terminate event instead.
     */
    protected function addToSearchIndex()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\FrontendTemplate::addToSearchIndex()" has been deprecated and will no longer work in Contao 5.0. Use the "kernel.terminate" event instead.');
    }

    /**
     * Return a custom layout section
     *
     * @param string $strKey The section name
     *
     * @return string The section markup
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use FrontendTemplate::section() instead.
     */
    public function getCustomSection($strKey)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\FrontendTemplate::getCustomSection()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\FrontendTemplate::section()" instead.');

        return '<div id="' . $strKey . '">' . $this->sections[$strKey] . '</div>' . "\n";
    }

    /**
     * Return all custom layout sections
     *
     * @param string $strKey An optional section name
     *
     * @return string The section markup
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use FrontendTemplate::sections() instead.
     */
    public function getCustomSections($strKey=null)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\FrontendTemplate::getCustomSections()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\FrontendTemplate::sections()" instead.');

        if ($strKey && !isset($this->positions[$strKey]))
        {
            return '';
        }

        $tag = 'div';

        // Use the section tag for the main column
        if ($strKey == 'main')
        {
            $tag = 'section';
        }

        $sections = '';

        // Standardize the IDs (thanks to Tsarma) (see #4251)
        foreach ($this->positions[$strKey] as $sect)
        {
            if (isset($this->sections[$sect['id']]))
            {
                $sections .= "\n" . '<' . $tag . ' id="' . StringUtil::standardize($sect['id'], true) . '">' . "\n" . '<div class="inside">' . "\n" . $this->sections[$sect['id']] . "\n" . '</div>' . "\n" . '</' . $tag . '>' . "\n";
            }
        }

        if (!$sections)
        {
            return '';
        }

        return '<div class="custom">' . "\n" . $sections . "\n" . '</div>' . "\n";
    }
```

```php
namespace Contao;

use Contao\CoreBundle\Security\ContaoCorePermissions;

class FrontendUser extends User
{
    /**
     * Symfony Security session key
     * @deprecated Deprecated since Contao 4.8, to be removed in Contao 5.0
     */
    const SECURITY_SESSION_KEY = '_security_contao_frontend';

    /**
     * Authenticate a user
     *
     * @return boolean
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    public function authenticate()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\FrontendUser::authenticate()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        return System::getContainer()->get('contao.security.token_checker')->hasFrontendUser();
    }

    /**
     * Try to log in the current user
     *
     * @return boolean True if the user could be logged in
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    public function login()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\FrontendUser::login()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        return System::getContainer()->get('contao.security.token_checker')->hasFrontendUser();
    }

    /**
     * Return true if the user is member of a particular group
     *
     * @param mixed $ids A single group ID or an array of group IDs
     *
     * @return boolean True if the user is a member of the group
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0;
     *             use Symfony security instead
     */
    public function isMemberOf($ids)
    {
        $security = System::getContainer()->get('security.helper');

        if ($security->getUser() === $this)
        {
            trigger_deprecation('contao/core-bundle', '4.12', 'Using "Contao\FrontendUser::isMemberOf()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

            return $security->isGranted(ContaoCorePermissions::MEMBER_IN_GROUPS, $ids);
        }

        return parent::isMemberOf($ids);
    }
```

```php
namespace Contao;

/**
 * Add system messages to the welcome screen.
 */
class Messages extends Backend
{
    /**
     * Check for the latest Contao version
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.
     */
    public function versionCheck()
    {
        trigger_deprecation('contao/core-bundle', '4.7', 'Using "Contao\Messages::versionCheck()" has been deprecated and will no longer work in Contao 5.0.');

        return '';
    }
```
```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.13', 'Using the "Contao\StyleSheets" class has been deprecated and will no longer work in Contao 5.0. Use external stylesheets instead.');

/**
 * Provide methods to handle style sheets.
 *
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use external stylesheets instead.
 */
class StyleSheets extends Backend
{
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.13', 'Using the "Contao\BackendFile" class has been deprecated and will no longer work in Contao 5.0. Use the picker instead.');

/**
 * Back end file picker.
 *
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use the picker instead.
 */
class BackendFile extends Backend
{
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.13', 'Using the "Contao\BackendPage" class has been deprecated and will no longer work in Contao 5.0. Use the picker instead.');

/**
 * Back end page picker.
 *
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use the picker instead.
 */
class BackendPage extends Backend
{
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.9', 'Using the "Contao\FrontendCron" class has been deprecated and will no longer work in Contao 5.0. Use the Contao\CoreBundle\Cron\Cron service instead.');

/**
 * Command scheduler controller.
 *
 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0; use the
 *             Contao\CoreBundle\Cron\Cron service instead
 */
class FrontendCron extends Frontend
{
```

```php
namespace Contao;

/**
 * Main front end controller.
 */
class FrontendIndex extends Frontend
{
    /**
     * Try to load the page from the cache
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the kernel.request event instead.
     */
    protected function outputFromCache()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\FrontendIndex::outputFromCache()" has been deprecated and will no longer work in Contao 5.0. Use the "kernel.request" event instead.');
    }
}
```

```php
/**
 * Provide miscellaneous methods that are used by the data configuration array.
 */
class tl_article extends Backend
{
    /**
     * @deprecated
     */
    public function pasteArticle(DataContainer $dc, $row, $table, $cr, $arrClipboard=null)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "tl_article::pasteArticle()" has been deprecated and will no longer work in Contao 5.0.');

        return System::getContainer()
            ->get('contao.listener.data_container.content_composition')
            ->renderArticlePasteButton($dc, $row, $table, $cr, $arrClipboard)
        ;
    }
}
```

```php
/**
 * Provide miscellaneous methods that are used by the data configuration array.
 */
class tl_content extends Backend
{
    /**
     * Return the edit article alias wizard
     *
     * @param DataContainer $dc
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function editArticleAlias(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Using "tl_content::editArticleAlias()" has been deprecated and will no longer work in Contao 5.0.');

        if ($dc->value < 1)
        {
            return '';
        }

        $title = sprintf($GLOBALS['TL_LANG']['tl_content']['editalias'], $dc->value);
        $href = System::getContainer()->get('router')->generate('contao_backend', array('do'=>'article', 'table'=>'tl_content', 'id'=>$dc->value, 'popup'=>'1', 'nb'=>'1', 'rt'=>REQUEST_TOKEN));

        return ' <a href="' . StringUtil::specialcharsUrl($href) . '" title="' . StringUtil::specialchars($title) . '" onclick="Backend.openModalIframe({\'title\':\'' . StringUtil::specialchars(str_replace("'", "\\'", $title)) . '\',\'url\':this.href});return false">' . Image::getHtml('alias.svg', $title) . '</a>';
    }

    /**
     * Get all articles and return them as array (article alias)
     *
     * @param DataContainer $dc
     *
     * @return array
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function getArticleAlias(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Using "tl_content::getArticleAlias()" has been deprecated and will no longer work in Contao 5.0.');

        $arrPids = array();
        $arrAlias = array();

        if (!$this->User->isAdmin)
        {
            foreach ($this->User->pagemounts as $id)
            {
                $arrPids[] = array($id);
                $arrPids[] = $this->Database->getChildRecords($id, 'tl_page');
            }

            if (!empty($arrPids))
            {
                $arrPids = array_merge(...$arrPids);
            }
            else
            {
                return $arrAlias;
            }

            $objAlias = $this->Database->prepare("SELECT a.id, a.pid, a.title, a.inColumn, p.title AS parent FROM tl_article a LEFT JOIN tl_page p ON p.id=a.pid WHERE a.pid IN(" . implode(',', array_map('\intval', array_unique($arrPids))) . ") AND a.id!=(SELECT pid FROM tl_content WHERE id=?) ORDER BY parent, a.sorting")
                                       ->execute($dc->id);
        }
        else
        {
            $objAlias = $this->Database->prepare("SELECT a.id, a.pid, a.title, a.inColumn, p.title AS parent FROM tl_article a LEFT JOIN tl_page p ON p.id=a.pid WHERE a.id!=(SELECT pid FROM tl_content WHERE id=?) ORDER BY parent, a.sorting")
                                       ->execute($dc->id);
        }

        if ($objAlias->numRows)
        {
            System::loadLanguageFile('tl_article');

            while ($objAlias->next())
            {
                $key = $objAlias->parent . ' (ID ' . $objAlias->pid . ')';
                $arrAlias[$key][$objAlias->id] = $objAlias->title . ' (' . ($GLOBALS['TL_LANG']['COLS'][$objAlias->inColumn] ?? $objAlias->inColumn) . ', ID ' . $objAlias->id . ')';
            }
        }

        return $arrAlias;
    }

    /**
     * Return the edit alias wizard
     *
     * @param DataContainer $dc
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function editAlias(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Using "tl_content::editAlias()" has been deprecated and will no longer work in Contao 5.0.');

        if ($dc->value < 1)
        {
            return '';
        }

        $title = sprintf($GLOBALS['TL_LANG']['tl_content']['editalias'], $dc->value);
        $href = System::getContainer()->get('router')->generate('contao_backend', array('do'=>'article', 'table'=>'tl_content', 'act'=>'edit', 'id'=>$dc->value, 'popup'=>'1', 'nb'=>'1', 'rt'=>REQUEST_TOKEN));

        return ' <a href="' . StringUtil::specialcharsUrl($href) . '" title="' . StringUtil::specialchars($title) . '" onclick="Backend.openModalIframe({\'title\':\'' . StringUtil::specialchars(str_replace("'", "\\'", $title)) . '\',\'url\':this.href});return false">' . Image::getHtml('alias.svg', $title) . '</a>';
    }

    /**
     * Get all content elements and return them as array (content element alias)
     *
     * @return array
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function getAlias()
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Using "tl_content::getAlias()" has been deprecated and will no longer work in Contao 5.0.');

        $arrPids = array();
        $arrAlias = array();

        if (!$this->User->isAdmin)
        {
            foreach ($this->User->pagemounts as $id)
            {
                $arrPids[] = array($id);
                $arrPids[] = $this->Database->getChildRecords($id, 'tl_page');
            }

            if (!empty($arrPids))
            {
                $arrPids = array_merge(...$arrPids);
            }
            else
            {
                return $arrAlias;
            }

            $objAlias = $this->Database->prepare("SELECT c.id, c.pid, c.type, (CASE c.type WHEN 'module' THEN m.name WHEN 'form' THEN f.title WHEN 'table' THEN c.summary ELSE c.headline END) AS headline, c.text, a.title FROM tl_content c LEFT JOIN tl_article a ON a.id=c.pid LEFT JOIN tl_module m ON m.id=c.module LEFT JOIN tl_form f on f.id=c.form WHERE a.pid IN(" . implode(',', array_map('\intval', array_unique($arrPids))) . ") AND (c.ptable='tl_article' OR c.ptable='') AND c.id!=? ORDER BY a.title, c.sorting")
                                       ->execute(Input::get('id'));
        }
        else
        {
            $objAlias = $this->Database->prepare("SELECT c.id, c.pid, c.type, (CASE c.type WHEN 'module' THEN m.name WHEN 'form' THEN f.title WHEN 'table' THEN c.summary ELSE c.headline END) AS headline, c.text, a.title FROM tl_content c LEFT JOIN tl_article a ON a.id=c.pid LEFT JOIN tl_module m ON m.id=c.module LEFT JOIN tl_form f on f.id=c.form WHERE (c.ptable='tl_article' OR c.ptable='') AND c.id!=? ORDER BY a.title, c.sorting")
                                       ->execute(Input::get('id'));
        }

        while ($objAlias->next())
        {
            $arrHeadline = StringUtil::deserialize($objAlias->headline, true);

            if (isset($arrHeadline['value']))
            {
                $headline = StringUtil::substr($arrHeadline['value'], 32);
            }
            else
            {
                $headline = StringUtil::substr(preg_replace('/[\n\r\t]+/', ' ', $arrHeadline[0]), 32);
            }

            $text = StringUtil::substr(strip_tags(preg_replace('/[\n\r\t]+/', ' ', $objAlias->text)), 32);
            $strText = ($GLOBALS['TL_LANG']['CTE'][$objAlias->type][0] ?? $objAlias->type) . ' (';

            if ($headline)
            {
                $strText .= $headline . ', ';
            }
            elseif ($text)
            {
                $strText .= $text . ', ';
            }

            $key = $objAlias->title . ' (ID ' . $objAlias->pid . ')';
            $arrAlias[$key][$objAlias->id] = $strText . 'ID ' . $objAlias->id . ')';
        }

        return $arrAlias;
    }
    /**
     * Return the edit article teaser wizard
     *
     * @param DataContainer $dc
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function editArticle(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Using "tl_content::editArticle()" has been deprecated and will no longer work in Contao 5.0.');

        if ($dc->value < 1)
        {
            return '';
        }

        $title = sprintf($GLOBALS['TL_LANG']['tl_content']['editarticle'], $dc->value);
        $href = System::getContainer()->get('router')->generate('contao_backend', array('do'=>'article', 'table'=>'tl_content', 'id'=>$dc->value, 'popup'=>'1', 'nb'=>'1', 'rt'=>REQUEST_TOKEN));

        return ' <a href="' . StringUtil::specialcharsUrl($href) . '" title="' . StringUtil::specialchars($title) . '" onclick="Backend.openModalIframe({\'title\':\'' . StringUtil::specialchars(str_replace("'", "\\'", $title)) . '\',\'url\':this.href});return false">' . Image::getHtml('alias.svg', $title) . '</a>';
    }

    /**
     * Get all articles and return them as array (article teaser)
     *
     * @param DataContainer $dc
     *
     * @return array
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public function getArticles(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'Using "tl_content::getArticles()" has been deprecated and will no longer work in Contao 5.0.');

        $arrPids = array();
        $arrArticle = array();
        $arrRoot = array();
        $intPid = $dc->activeRecord->pid ?? null;

        if (Input::get('act') == 'overrideAll')
        {
            $intPid = Input::get('id');
        }

        // Limit pages to the website root
        $objArticle = $this->Database->prepare("SELECT pid FROM tl_article WHERE id=?")
                                     ->limit(1)
                                     ->execute($intPid);

        if ($objArticle->numRows)
        {
            $objPage = PageModel::findWithDetails($objArticle->pid);
            $arrRoot = $this->Database->getChildRecords($objPage->rootId, 'tl_page');
            array_unshift($arrRoot, $objPage->rootId);
        }

        unset($objArticle);

        // Limit pages to the user's pagemounts
        if ($this->User->isAdmin)
        {
            $objArticle = $this->Database->execute("SELECT a.id, a.pid, a.title, a.inColumn, p.title AS parent FROM tl_article a LEFT JOIN tl_page p ON p.id=a.pid" . (!empty($arrRoot) ? " WHERE a.pid IN(" . implode(',', array_map('\intval', array_unique($arrRoot))) . ")" : "") . " ORDER BY parent, a.sorting");
        }
        else
        {
            foreach ($this->User->pagemounts as $id)
            {
                if (!in_array($id, $arrRoot))
                {
                    continue;
                }

                $arrPids[] = array($id);
                $arrPids[] = $this->Database->getChildRecords($id, 'tl_page');
            }

            if (!empty($arrPids))
            {
                $arrPids = array_merge(...$arrPids);
            }
            else
            {
                return $arrArticle;
            }

            $objArticle = $this->Database->execute("SELECT a.id, a.pid, a.title, a.inColumn, p.title AS parent FROM tl_article a LEFT JOIN tl_page p ON p.id=a.pid WHERE a.pid IN(" . implode(',', array_map('\intval', array_unique($arrPids))) . ") ORDER BY parent, a.sorting");
        }

        // Edit the result
        if ($objArticle->numRows)
        {
            System::loadLanguageFile('tl_article');

            while ($objArticle->next())
            {
                $key = $objArticle->parent . ' (ID ' . $objArticle->pid . ')';
                $arrArticle[$key][$objArticle->id] = $objArticle->title . ' (' . ($GLOBALS['TL_LANG']['COLS'][$objArticle->inColumn] ?? $objArticle->inColumn) . ', ID ' . $objArticle->id . ')';
            }
        }

        return $arrArticle;
    }

    /**
     * Return the link picker wizard
     *
     * @param DataContainer $dc
     *
     * @return string
     *
     * @deprecated Deprecated since Contao 4.4, to be removed in Contao 5.
     *             Set the "dcaPicker" eval attribute instead.
     */
    public function pagePicker(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.4', 'Using "tl_content::pagePicker()" has been deprecated and will no longer work in Contao 5.0. Set the "dcaPicker" eval attribute instead.');

        return Backend::getDcaPickerWizard(true, $dc->table, $dc->field, $dc->inputName);
    }
```

```php
/**
 * Provide miscellaneous methods that are used by the data configuration array.
 */
class tl_page extends Backend
{
    /**
     * Make sure that top-level pages are root pages
     *
     * @param mixed         $varValue
     * @param DataContainer $dc
     *
     * @return mixed
     *
     * @throws Exception
     *
     * @deprecated
     */
    public function checkRootType($varValue, DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "tl_page::checkRootType()" has been deprecated and will no longer work in Contao 5.0.');

        if ($varValue != 'root' && $dc->activeRecord->pid == 0)
        {
            throw new Exception($GLOBALS['TL_LANG']['ERR']['topLevelRoot']);
        }

        return $varValue;
    }

    /**
     * Automatically create an article in the main column of a new page
     *
     * @param DataContainer $dc
     *
     * @deprecated
     */
    public function generateArticle(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "tl_page::generateArticle()" has been deprecated and will no longer work in Contao 5.0.');

        System::getContainer()
            ->get('contao.listener.data_container.content_composition')
            ->generateArticleForPage($dc)
        ;
    }

    /**
     * Purge the search index if a page is being deleted
     *
     * @param DataContainer $dc
     *
     * @deprecated
     */
    public function purgeSearchIndex(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "tl_page::purgeSearchIndex()" has been deprecated and will no longer work in Contao 5.0.');

        System::getContainer()
            ->get('contao.listener.data_container.page_search')
            ->onDelete($dc)
        ;
    }

    /**
     * Returns all allowed page types as array
     *
     * @param DataContainer $dc
     *
     * @return array
     *
     * @deprecated
     */
    public function getPageTypes(DataContainer $dc)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "tl_page::getPageTypes()" has been deprecated and will no longer work in Contao 5.0.');

        return System::getContainer()->get('contao.listener.data_container.page_type_options')($dc);
    }

    /**
     * Generate an "edit articles" button and return it as string
     *
     * @param array  $row
     * @param string $href
     * @param string $label
     * @param string $title
     * @param string $icon
     *
     * @return string
     *
     * @deprecated
     */
    public function editArticles($row, $href, $label, $title, $icon)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "tl_page::editArticles()" has been deprecated and will no longer work in Contao 5.0.');

        return System::getContainer()
            ->get('contao.listener.data_container.content_composition')
            ->renderPageArticlesOperation($row, $href, $label, $title, $icon)
        ;
    }
```

```php
namespace Contao;

class DC_Folder extends DataContainer implements ListableDataContainerInterface, EditableDataContainerInterface
{
/**
     * Protect a folder
     *
     * @throws InternalServerErrorException
     *
     * @deprecated Deprecated since Contao 4.7 to be removed in 5.0.
     *             Use Contao\Folder::protect() and Contao\Folder::unprotect() instead.
     */
    public function protect()
    {
        trigger_deprecation('contao/core-bundle', '4.7', 'Using "Contao\DC_Folder::protect()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Folder::protect()" and "Contao\Folder::unprotect()" instead.');

        if (!is_dir($this->strRootDir . '/' . $this->intId))
        {
            throw new InternalServerErrorException('Resource "' . $this->intId . '" is not a directory.');
        }

        // Protect or unprotect the folder
        if (is_file($this->strRootDir . '/' . $this->intId . '/.public'))
        {
            $objFolder = new Folder($this->intId);
            $objFolder->protect();

            $this->import(Automator::class, 'Automator');
            $this->Automator->generateSymlinks();

            System::getContainer()->get('monolog.logger.contao.files')->info('Folder "' . $this->intId . '" has been protected');
        }
        else
        {
            $objFolder = new Folder($this->intId);
            $objFolder->unprotect();

            $this->import(Automator::class, 'Automator');
            $this->Automator->generateSymlinks();

            System::getContainer()->get('monolog.logger.contao.files')->info('The protection from folder "' . $this->intId . '" has been removed');
        }

        $this->redirect($this->getReferer());
    }
```

```php
namespace Contao;

class Form extends Hybrid
{
    /**
     * Get the maximum file size that is allowed for file uploads
     *
     * @return integer
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use $this->objModel->getMaxUploadFileSize() instead.
     */
    protected function getMaxFileSize()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Form::getMaxFileSize()" has been deprecated and will no longer work in Contao 5.0. Use "$this->objModel->getMaxUploadFileSize()" instead.');

        return $this->objModel->getMaxUploadFileSize();
    }
```

```php
namespace Contao;

class FormPassword extends Widget
{
    /**
     * Generate the label of the confirmation field and return it as string
     *
     * @return string The confirmation label markup
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0
     */
    public function generateConfirmationLabel()
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using "Contao\FormPassword::generateConfirmation()" has been deprecated and will no longer work in Contao 5.0.');

        return sprintf(
            '<label for="ctrl_%s_confirm" class="confirm%s">%s%s%s</label>',
            $this->strId,
            ($this->strClass ? ' ' . $this->strClass : ''),
            ($this->mandatory ? '<span class="invisible">' . $GLOBALS['TL_LANG']['MSC']['mandatory'] . ' </span>' : ''),
            sprintf($GLOBALS['TL_LANG']['MSC']['confirm'][0], $this->strLabel),
            ($this->mandatory ? '<span class="mandatory">*</span>' : '')
        );
    }

    /**
     * Generate the widget and return it as string
     *
     * @return string The confirmation field markup
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0
     */
    public function generateConfirmation()
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using "Contao\FormPassword::generateConfirmation()" has been deprecated and will no longer work in Contao 5.0.');

        return sprintf(
            '<input type="password" name="%s_confirm" id="ctrl_%s_confirm" class="text password confirm%s" value="" autocomplete="new-password"%s%s',
            $this->strName,
            $this->strId,
            ($this->strClass ? ' ' . $this->strClass : ''),
            $this->getAttributes(),
            $this->strTagEnding
        );
    }
```

```php
/**
 * Class UnresolvableDependenciesException
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 */
class UnresolvableDependenciesException extends Exception
{
}
```

```php
/**
 * Add a log entry
 *
 * @param string $strMessage
 * @param string $strLog
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use the logger service instead.
 */
function log_message($strMessage, $strLog=null)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "log_message()" has been deprecated and will no longer work in Contao 5.0. Use the logger service instead.');

    if ($strLog === null)
    {
        $strLog = 'prod-' . date('Y-m-d') . '.log';
    }

    $strLogsDir = null;

    if (($container = System::getContainer()) !== null)
    {
        $strLogsDir = $container->getParameter('kernel.logs_dir');
    }

    if (!$strLogsDir)
    {
        $strLogsDir = $container->getParameter('kernel.project_dir') . '/var/logs';
    }

    error_log(sprintf("[%s] %s\n", date('d-M-Y H:i:s'), $strMessage), 3, $strLogsDir . '/' . $strLog);
}

/**
 * Scan a directory and return its files and folders as array
 *
 * @param string  $strFolder
 * @param boolean $blnUncached
 *
 * @return array
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function scan($strFolder, $blnUncached=false)
{
    trigger_deprecation('contao/core-bundle', '4.10', 'Using "scan()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Folder::scan()" instead.');

    return Folder::scan($strFolder, $blnUncached);
}

/**
 * Convert special characters to HTML entities and make sure that
 * entities are never double converted.
 *
 * @param string  $strString
 * @param boolean $blnStripInsertTags
 *
 * @return string
 *
 * @deprecated Using specialchars() has been deprecated and will no longer work in Contao 5.0.
 *             Use StringUtil::specialchars() instead.
 */
function specialchars($strString, $blnStripInsertTags=false)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "specialchars()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::specialchars()" instead.');

    if ($blnStripInsertTags)
    {
        $strString = strip_insert_tags($strString);
    }

    return htmlspecialchars($strString, ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML5, System::getContainer()->getParameter('kernel.charset'), false);
}

/**
 * Standardize a parameter (strip special characters and convert spaces)
 *
 * @param string  $strString
 * @param boolean $blnPreserveUppercase
 *
 * @return string
 *
 * @deprecated Using standardize() has been deprecated and will no longer work in Contao 5.0.
 *             Use StringUtil::standardize() instead.
 */
function standardize($strString, $blnPreserveUppercase=false)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "standardize()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::standardize()" instead.');

    $arrSearch = array('/[^\pN\pL \.\&\/_-]+/u', '/[ \.\&\/-]+/');
    $arrReplace = array('', '-');

    $strString = html_entity_decode($strString, ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML5, System::getContainer()->getParameter('kernel.charset'));
    $strString = strip_insert_tags($strString);
    $strString = preg_replace($arrSearch, $arrReplace, $strString);

    if (is_numeric(substr($strString, 0, 1)))
    {
        $strString = 'id-' . $strString;
    }

    if (!$blnPreserveUppercase)
    {
        $strString = mb_strtolower($strString);
    }

    return trim($strString, '-');
}

/**
 * Remove Contao insert tags from a string
 *
 * @param string $strString
 *
 * @return string
 *
 * @deprecated Using strip_insert_tags() has been deprecated and will no longer work in Contao 5.0.
 *             Use StringUtil::stripInsertTags() instead.
 */
function strip_insert_tags($strString)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "strip_insert_tags()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::stripInsertTags()" instead.');

    $count = 0;

    do
    {
        $strString = preg_replace('/{{[^{}]*}}/', '', $strString, -1, $count);
    }
    while ($count > 0);

    return $strString;
}

/**
 * Return an unserialized array or the argument
 *
 * @param mixed   $varValue
 * @param boolean $blnForceArray
 *
 * @return mixed
 *
 * @deprecated Using deserialize() has been deprecated and will no longer work in Contao 5.0.
 *             Use StringUtil::deserialize() instead.
 */
function deserialize($varValue, $blnForceArray=false)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "deserialize()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::deserialize()" instead.');

    // Already an array
    if (is_array($varValue))
    {
        return $varValue;
    }

    // Null
    if ($varValue === null)
    {
        return $blnForceArray ? array() : null;
    }

    // Not a string
    if (!is_string($varValue))
    {
        return $blnForceArray ? array($varValue) : $varValue;
    }

    // Empty string
    if (trim($varValue) === '')
    {
        return $blnForceArray ? array() : '';
    }

    // Potentially including an object (see #6724)
    if (preg_match('/[OoC]:\+?[0-9]+:"/', $varValue))
    {
        trigger_error('The deserialize() function does not allow serialized objects', E_USER_WARNING);

        return $blnForceArray ? array($varValue) : $varValue;
    }

    $varUnserialized = @unserialize($varValue, array('allowed_classes' => false));

    if (is_array($varUnserialized))
    {
        $varValue = $varUnserialized;
    }
    elseif ($blnForceArray)
    {
        $varValue = array($varValue);
    }

    return $varValue;
}

/**
 * Split a string into fragments, remove whitespace and return fragments as array
 *
 * @param string $strPattern
 * @param string $strString
 *
 * @return array
 *
 * @deprecated Using trimsplit() has been deprecated and will no longer work in Contao 5.0.
 *             Use StringUtil::trimsplit() instead.
 */
function trimsplit($strPattern, $strString)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "trimsplit()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::trimsplit()" instead.');

    // Split
    if (strlen($strPattern) == 1)
    {
        $arrFragments = array_map('trim', explode($strPattern, $strString));
    }
    else
    {
        $arrFragments = array_map('trim', preg_split('/' . $strPattern . '/ui', $strString));
    }

    // Empty array
    if (count($arrFragments) < 2 && !strlen($arrFragments[0]))
    {
        $arrFragments = array();
    }

    return $arrFragments;
}

/**
 * Convert all ampersands into their HTML entity (default) or unencoded value
 *
 * @param string  $strString
 * @param boolean $blnEncode
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function ampersand($strString, $blnEncode=true)
{
    trigger_deprecation('contao/core-bundle', '4.10', 'Using "ampersand()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::ampersand()" instead.');

    return StringUtil::ampersand($strString, $blnEncode);
}

/**
 * Replace line breaks with HTML5-style <br> tags
 *
 * @param string  $str
 * @param boolean $xhtml
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function nl2br_html5($str, $xhtml=false)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "nl2br_html5()" has been deprecated and will no longer work in Contao 5.0.');

    return nl2br($str, $xhtml);
}

/**
 * Replace line breaks with XHTML-style <br /> tags
 *
 * @param string $str
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function nl2br_xhtml($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "nl2br_xhtml()" has been deprecated and will no longer work in Contao 5.0.');

    return nl2br($str);
}

/**
 * Replace line breaks with <br> tags preserving preformatted text
 *
 * @param string  $str
 * @param boolean $xhtml
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function nl2br_pre($str, $xhtml=false)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "nl2br_pre()" has been deprecated and will no longer work in Contao 5.0.');

    return preg_replace('/\r?\n/', $xhtml ? '<br />' : '<br>', $str);
}

/**
 * Compare two file names using a case-insensitive "natural order" algorithm
 *
 * @param string $a
 * @param string $b
 *
 * @return integer
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function basename_natcasecmp($a, $b)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "basename_natcasecmp()" has been deprecated and will no longer work in Contao 5.0.');

    return strnatcasecmp(basename($a), basename($b));
}

/**
 * Compare two file names using a case-insensitive, reverse "natural order" algorithm
 *
 * @param string $a
 * @param string $b
 *
 * @return integer
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function basename_natcasercmp($a, $b)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "basename_natcasercmp()" has been deprecated and will no longer work in Contao 5.0.');

    return -strnatcasecmp(basename($a), basename($b));
}

/**
 * Sort an array by keys using a case-insensitive "natural order" algorithm
 *
 * @param array $arrArray
 *
 * @return array
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function natcaseksort($arrArray)
{
    trigger_deprecation('contao/core-bundle', '4.10', 'Using "natcaseksort()" has been deprecated and will no longer work in Contao 5.0. Use "uksort()" with "strnatcasecmp" instead.');

    uksort($arrArray, 'strnatcasecmp');

    return $arrArray;
}

/**
 * Compare two values based on their length (ascending)
 *
 * @param integer $a
 * @param integer $b
 *
 * @return integer
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function length_sort_asc($a, $b)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "length_sort_asc()" has been deprecated and will no longer work in Contao 5.0. Use a closure instead.');

    return strlen($a) - strlen($b);
}

/**
 * Compare two values based on their length (descending)
 *
 * @param integer $a
 * @param integer $b
 *
 * @return integer
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function length_sort_desc($a, $b)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "length_sort_desc()" has been deprecated and will no longer work in Contao 5.0. Use a closure instead.');

    return strlen($b) - strlen($a);
}

/**
 * Insert a parameter or array into an existing array at a particular index
 *
 * @param array   $arrCurrent
 * @param integer $intIndex
 * @param mixed   $arrNew
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function array_insert(&$arrCurrent, $intIndex, $arrNew)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "array_insert()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\ArrayUtil::arrayInsert()" instead.');

    ArrayUtil::arrayInsert($arrCurrent, $intIndex, $arrNew);
}

/**
 * Duplicate a particular element of an array
 *
 * @param array   $arrStack
 * @param integer $intIndex
 *
 * @return array
 *
 * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
 */
function array_duplicate($arrStack, $intIndex)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "array_duplicate()" has been deprecated and will no longer work in Contao 5.0.');

    $arrBuffer = $arrStack;
    $arrStack = array();

    for ($i=0; $i<=$intIndex; $i++)
    {
        $arrStack[] = $arrBuffer[$i];
    }

    for ($i=$intIndex, $c=count($arrBuffer); $i<$c; $i++)
    {
        $arrStack[] = $arrBuffer[$i];
    }

    return $arrStack;
}

/**
 * Move an array element one position up
 *
 * @param array   $arrStack
 * @param integer $intIndex
 *
 * @return array
 *
 * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
 */
function array_move_up($arrStack, $intIndex)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "array_move_up()" has been deprecated and will no longer work in Contao 5.0.');

    if ($intIndex > 0)
    {
        $arrBuffer = $arrStack[$intIndex];
        $arrStack[$intIndex] = $arrStack[($intIndex-1)];
        $arrStack[($intIndex-1)] = $arrBuffer;
    }
    else
    {
        $arrStack[] = $arrStack[$intIndex];
        array_shift($arrStack);
    }

    return $arrStack;
}

/**
 * Move an array element one position down
 *
 * @param array   $arrStack
 * @param integer $intIndex
 *
 * @return array
 *
 * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
 */
function array_move_down($arrStack, $intIndex)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "array_move_down()" has been deprecated and will no longer work in Contao 5.0.');

    if (($intIndex+1) < count($arrStack))
    {
        $arrBuffer = $arrStack[$intIndex];
        $arrStack[$intIndex] = $arrStack[($intIndex+1)];
        $arrStack[($intIndex+1)] = $arrBuffer;
    }
    else
    {
        array_unshift($arrStack, $arrStack[$intIndex]);
        array_pop($arrStack);
    }

    return $arrStack;
}

/**
 * Delete a particular element of an array
 *
 * @param array   $arrStack
 * @param integer $intIndex
 *
 * @return array
 *
 * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
 */
function array_delete($arrStack, $intIndex)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "array_delete()" has been deprecated and will no longer work in Contao 5.0.');

    unset($arrStack[$intIndex]);

    return array_values($arrStack);
}

/**
 * Return true if an array is associative
 *
 * @param array $arrArray
 *
 * @return boolean
 *
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 */
function array_is_assoc($arrArray)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "array_is_assoc()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\ArrayUtil::isAssoc()" instead.');

    return ArrayUtil::isAssoc($arrArray);
}

/**
 * Return a specific character
 *
 * Unicode version of chr() that handles UTF-8 characters.
 *
 * @param integer $dec
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_chr() instead.
 */
function utf8_chr($dec)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_chr()" has been deprecated and will no longer work in Contao 5.0. Use "mb_chr()" instead.');

    return mb_chr($dec);
}

/**
 * Return the ASCII value of a character
 *
 * Unicode version of ord() that handles UTF-8 characters.
 *
 * @param string $str
 *
 * @return integer
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_ord() instead.
 */
function utf8_ord($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_ord()" has been deprecated and will no longer work in Contao 5.0. Use "mb_ord()" instead.');

    return mb_ord($str);
}

/**
 * Convert character encoding
 *
 * @param string $str
 * @param string $to
 * @param string $from
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use StringUtil::convertEncoding() instead.
 */
function utf8_convert_encoding($str, $to, $from=null)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_convert_encoding()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::convertEncoding()" instead.');

    if (!$str)
    {
        return '';
    }

    if (!$from)
    {
        $from = mb_detect_encoding($str);
    }

    if ($from == $to)
    {
        return $str;
    }

    if ($from == 'UTF-8' && $to == 'ISO-8859-1')
    {
        return utf8_decode($str);
    }

    if ($from == 'ISO-8859-1' && $to == 'UTF-8')
    {
        return utf8_encode($str);
    }

    return mb_convert_encoding($str, $to, $from);
}

/**
 * Convert all unicode entities to their applicable characters
 *
 * Calls mb_chr() to convert unicode entities. HTML entities like '&nbsp;'
 * or '&quot;' will not be decoded.
 *
 * @param string $str
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use html_entity_decode() instead.
 */
function utf8_decode_entities($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_decode_entities()" has been deprecated and will no longer work in Contao 5.0. Use "html_entity_decode()" instead.');

    $str = preg_replace_callback('~&#x([0-9a-f]+);~i', static function ($matches) { return mb_chr(hexdec($matches[1])); }, $str);
    $str = preg_replace_callback('~&#([0-9]+);~', static function ($matches) { return mb_chr($matches[1]); }, $str);

    return $str;
}

/**
 * Callback function for utf8_decode_entities
 *
 * @param array $matches
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 */
function utf8_chr_callback($matches)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_chr_callback()" has been deprecated and will no longer work in Contao 5.0.');

    return mb_chr($matches[1]);
}

/**
 * Callback function for utf8_decode_entities
 *
 * @param array $matches
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 */
function utf8_hexchr_callback($matches)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_hexchr_callback()" has been deprecated and will no longer work in Contao 5.0.');

    return mb_chr(hexdec($matches[1]));
}

/**
 * Detect the encoding of a string
 *
 * @param string $str
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_detect_encoding() instead.
 */
function utf8_detect_encoding($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_detect_encoding()" has been deprecated and will no longer work in Contao 5.0. Use "mb_detect_encoding()" instead.');

    return mb_detect_encoding($str, array('ASCII', 'ISO-2022-JP', 'UTF-8', 'EUC-JP', 'ISO-8859-1'));
}

/**
 * Romanize a string
 *
 * @param string $str
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use the symfony/string component instead.
 */
function utf8_romanize($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_romanize()" has been deprecated and will no longer work in Contao 5.0. Use the "symfony/string" component instead.');

    return (new UnicodeString($str))->ascii()->toString();
}

/**
 * Determine the number of characters of a string
 *
 * @param string $str
 *
 * @return integer
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_strlen() instead.
 */
function utf8_strlen($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_strlen()" has been deprecated and will no longer work in Contao 5.0. Use "mb_strlen()" instead.');

    return mb_strlen($str);
}

/**
 * Find the position of the first occurrence of a string in another string
 *
 * @param string  $haystack
 * @param string  $needle
 * @param integer $offset
 *
 * @return integer
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_strpos instead.
 */
function utf8_strpos($haystack, $needle, $offset=0)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_strpos()" has been deprecated and will no longer work in Contao 5.0. Use "mb_strpos()" instead.');

    return mb_strpos($haystack, $needle, $offset);
}

/**
 * Find the last occurrence of a character in a string
 *
 * @param string $haystack
 * @param string $needle
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_strrchr() instead.
 */
function utf8_strrchr($haystack, $needle)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_strrchr()" has been deprecated and will no longer work in Contao 5.0. Use "mb_strrchr()" instead.');

    return mb_strrchr($haystack, $needle);
}

/**
 * Find the position of the last occurrence of a string in another string
 *
 * @param string $haystack
 * @param string $needle
 *
 * @return mixed
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_strrpos() instead.
 */
function utf8_strrpos($haystack, $needle)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_strrpos()" has been deprecated and will no longer work in Contao 5.0. Use "mb_strrpos()" instead.');

    return mb_strrpos($haystack, $needle);
}

/**
 * Find the first occurrence of a string in another string
 *
 * @param string $haystack
 * @param string $needle
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_strstr() instead.
 */
function utf8_strstr($haystack, $needle)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_strstr()" has been deprecated and will no longer work in Contao 5.0. Use "mb_strstr()" instead.');

    return mb_strstr($haystack, $needle);
}

/**
 * Make a string lowercase
 *
 * @param string $str
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_strtolower() instead.
 */
function utf8_strtolower($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_strtolower()" has been deprecated and will no longer work in Contao 5.0. Use "mb_strtolower()" instead.');

    return mb_strtolower($str);
}

/**
 * Make a string uppercase
 *
 * @param string $str
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_strtoupper() instead.
 */
function utf8_strtoupper($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_strtoupper()" has been deprecated and will no longer work in Contao 5.0. Use "mb_strtoupper()" instead.');

    return mb_strtoupper($str);
}

/**
 * Return substring of a string
 *
 * @param string  $str
 * @param integer $start
 * @param integer $length
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_substr() instead.
 */
function utf8_substr($str, $start, $length=null)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_substr()" has been deprecated and will no longer work in Contao 5.0. Use "mb_substr()" instead.');

    return mb_substr($str, $start, $length);
}

/**
 * Make sure the first letter is uppercase
 *
 * @param string $str
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use the symfony/string component instead.
 */
function utf8_ucfirst($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_ucfirst()" has been deprecated and will no longer work in Contao 5.0. Use the "symfony/string" component instead.');

    return (new UnicodeString($str))->title()->toString();
}

/**
 * Convert a string to an array
 *
 * @param string $str
 *
 * @return array
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use mb_str_split() instead.
 */
function utf8_str_split($str)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "utf8_str_split()" has been deprecated and will no longer work in Contao 5.0. Use "mb_str_split()" instead.');

    return mb_str_split($str);
}

/**
 * Replace line breaks with <br> tags (to be used with preg_replace_callback)
 *
 * @param array $matches
 *
 * @return string
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 */
function nl2br_callback($matches)
{
    trigger_deprecation('contao/core-bundle', '4.0', 'Using "nl2br_callback()" has been deprecated and will no longer work in Contao 5.0.');

    return str_replace("\n", '<br>', $matches[0]);
}
```
```php
namespace Contao;

class Automator extends System
{
    /**
     * Purge the search cache
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0.
     */
    public function purgeSearchCache()
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using "Contao\Automator::purgeSearchCache()" has been deprecated and will no longer work in Contao 5.0.');

        $strCacheDir = StringUtil::stripRootDir(System::getContainer()->getParameter('kernel.cache_dir'));

        $objFolder = new Folder($strCacheDir . '/contao/search');
        $objFolder->purge();

        System::getContainer()->get('monolog.logger.contao.cron')->info('Purged the search cache');
    }

/**
     * Rotate the log files
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the logger service instead, which rotates its log files automatically.
     */
    public function rotateLogs()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Automator::rotateLogs()" has been deprecated and will no longer work in Contao 5.0. Use the logger service instead, which rotates its log files automatically.');

        $projectDir = System::getContainer()->getParameter('kernel.project_dir');
        $arrFiles = preg_grep('/\.log$/', Folder::scan($projectDir . '/system/logs'));

        foreach ($arrFiles as $strFile)
        {
            // Ignore Monolog log files (see #2579)
            if (preg_match('/-\d{4}-\d{2}-\d{2}\.log$/', $strFile))
            {
                continue;
            }

            $objFile = new File('system/logs/' . $strFile . '.9');

            // Delete the oldest file
            if ($objFile->exists())
            {
                $objFile->delete();
            }

            // Rotate the files (e.g. error.log.4 becomes error.log.5)
            for ($i=8; $i>0; $i--)
            {
                $strGzName = 'system/logs/' . $strFile . '.' . $i;

                if (file_exists($projectDir . '/' . $strGzName))
                {
                    $objFile = new File($strGzName);
                    $objFile->renameTo('system/logs/' . $strFile . '.' . ($i+1));
                }
            }

            // Add .1 to the latest file
            $objFile = new File('system/logs/' . $strFile);
            $objFile->renameTo('system/logs/' . $strFile . '.1');
        }
    }
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.13', 'Using the Cache library is deprecated and will no longer work in Contao 5.0. Use your own in-memory cache instead.');

/**
 * A static class to store non-persistent data
 *
 * The class functions as a global cache container where you can store data
 * that is reused by the application. The cache content is not persisted, so
 * once the process is completed, the data is gone.
 *
 * Usage:
 *
 *     public function getResult()
 *     {
 *         if (!Cache::has('result'))
 *         {
 *             Cache::set('result') = $this->complexMethod();
 *         }
 *         return Cache::get('result');
 *     }
 *
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0;
 *             use your own in-memory cache instead
 */
class Cache
{
    /**
     * Object instance (Singleton)
     * @var Cache
     */
    protected static $objInstance;

    /**
     * The cache data
     * @var array
     */
    protected static $arrData = array();

    /**
     * Check whether a key is set
     *
     * @param string $strKey The cache key
     *
     * @return boolean True if the key is set
     */
    public static function has($strKey)
    {
        return isset(static::$arrData[$strKey]);
    }

    /**
     * Return a cache entry
     *
     * @param string $strKey The cache key
     *
     * @return mixed The cached data
     */
    public static function get($strKey)
    {
        return static::$arrData[$strKey];
    }

    /**
     * Add a cache entry
     *
     * @param string $strKey   The cache key
     * @param mixed  $varValue The data to be cached
     */
    public static function set($strKey, $varValue)
    {
        static::$arrData[$strKey] = $varValue;
    }

    /**
     * Remove a cache entry
     *
     * @param string $strKey The cache key
     */
    public static function remove($strKey)
    {
        unset(static::$arrData[$strKey]);
    }

    /**
     * Prevent direct instantiation (Singleton)
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Cache class is now static.
     */
    protected function __construct()
    {
    }

    /**
     * Prevent cloning of the object (Singleton)
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Cache class is now static.
     */
    final public function __clone()
    {
    }

    /**
     * Check whether a key is set
     *
     * @param string $strKey The cache key
     *
     * @return boolean True if the key is set
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Cache::has() instead.
     */
    public function __isset($strKey)
    {
        return static::has($strKey);
    }

    /**
     * Return a cache entry
     *
     * @param string $strKey The cache key
     *
     * @return mixed|null The cached data
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Cache::get() instead.
     */
    public function __get($strKey)
    {
        if (static::has($strKey))
        {
            return static::get($strKey);
        }

        return null;
    }

    /**
     * Add a cache entry
     *
     * @param string $strKey   The cache key
     * @param mixed  $varValue The data to be stored
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Cache::set() instead.
     */
    public function __set($strKey, $varValue)
    {
        static::set($strKey, $varValue);
    }

    /**
     * Remove a cache entry
     *
     * @param string $strKey The cache key
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Cache::remove() instead.
     */
    public function __unset($strKey)
    {
        static::remove($strKey);
    }

    /**
     * Instantiate the cache object (Factory)
     *
     * @return Cache The object instance
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Cache class is now static.
     */
    public static function getInstance()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Cache::getInstance()" has been deprecated and will no longer work in Contao 5.0. The "Contao\Cache" class is now static.');

        if (static::$objInstance === null)
        {
            static::$objInstance = new static();
        }

        return static::$objInstance;
    }
}

class_alias(Cache::class, 'Cache');
```

```php
namespace Contao;

/**
 * Automatically loads class files based on a mapper array
 *
 * The class stores namespaces and classes and automatically loads the class
 * files upon their first usage. It uses a mapper array to support complex
 * nesting and arbitrary subfolders to store the class files in.
 *
 * Usage:
 *
 *     ClassLoader::addNamespace('Custom');
 *     ClassLoader::addClass('Custom\Calendar', 'calendar/Calendar.php');
 *
 * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
 *             Use the Composer autoloader instead.
 */
class ClassLoader
{
    /**
     * Known namespaces
     * @var array
     */
    protected static $namespaces = array('Contao');

    /**
     * Known classes
     * @var array
     */
    protected static $classes = array();

    /**
     * Add a new namespace
     *
     * @param string $name The namespace name
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
     */
    public static function addNamespace($name)
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\ClassLoader::addNamespace()" has been deprecated and will no longer work in Contao 5.0.');

        if (\in_array($name, self::$namespaces))
        {
            return;
        }

        array_unshift(self::$namespaces, $name);
    }

    /**
     * Add multiple new namespaces
     *
     * @param array $names An array of namespace names
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
     */
    public static function addNamespaces($names)
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\ClassLoader::addNamespaces()" has been deprecated and will no longer work in Contao 5.0.');

        foreach ($names as $name)
        {
            self::addNamespace($name);
        }
    }

    /**
     * Return the namespaces as array
     *
     * @return array An array of all namespaces
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
     */
    public static function getNamespaces()
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\ClassLoader::getNamespaces()" has been deprecated and will no longer work in Contao 5.0.');

        return self::$namespaces;
    }

    /**
     * Add a new class with its file path
     *
     * @param string $class The class name
     * @param string $file  The path to the class file
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
     */
    public static function addClass($class, $file)
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\ClassLoader::addClass()" has been deprecated and will no longer work in Contao 5.0.');

        self::$classes[$class] = $file;
    }

    /**
     * Add multiple new classes with their file paths
     *
     * @param array $classes An array of classes
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
     */
    public static function addClasses($classes)
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\ClassLoader::addClasses()" has been deprecated and will no longer work in Contao 5.0.');

        foreach ($classes as $class=>$file)
        {
            self::addClass($class, $file);
        }
    }

    /**
     * Return the classes as array.
     *
     * @return array An array of all classes
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
     */
    public static function getClasses()
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\ClassLoader::getClasses()" has been deprecated and will no longer work in Contao 5.0.');

        return self::$classes;
    }

    /**
     * Autoload a class and create an alias in the global namespace
     *
     * To preserve backwards compatibility with Contao 2 extensions, all core
     * classes will be aliased into the global namespace.
     *
     * @param string $class The class name
     */
    public static function load($class)
    {
        if (class_exists($class, false) || interface_exists($class, false) || trait_exists($class, false))
        {
            return;
        }

        // The class file is set in the mapper
        if (isset(self::$classes[$class]))
        {
            if (System::getContainer()->getParameter('kernel.debug'))
            {
                $GLOBALS['TL_DEBUG']['classes_set'][$class] = $class;
            }

            include System::getContainer()->getParameter('kernel.project_dir') . '/' . self::$classes[$class];
        }

        // Find the class in the registered namespaces
        elseif (($namespaced = self::findClass($class)) !== null)
        {
            if (!class_exists($namespaced, false) && !interface_exists($namespaced, false) && !trait_exists($namespaced, false))
            {
                if (System::getContainer()->getParameter('kernel.debug'))
                {
                    $GLOBALS['TL_DEBUG']['classes_aliased'][$class] = $namespaced;
                }

                include System::getContainer()->getParameter('kernel.project_dir') . '/' . self::$classes[$namespaced];
            }

            class_alias($namespaced, $class);
        }

        // Try to map the class to a Contao class loaded via Composer
        elseif (strncmp($class, 'Contao\\', 7) !== 0)
        {
            $namespaced = 'Contao\\' . $class;

            if (class_exists($namespaced) || interface_exists($namespaced) || trait_exists($namespaced))
            {
                if (System::getContainer()->getParameter('kernel.debug'))
                {
                    $GLOBALS['TL_DEBUG']['classes_composerized'][$class] = $namespaced;
                }

                if (!class_exists($class, false) && !interface_exists($class, false) && !trait_exists($class, false))
                {
                    class_alias($namespaced, $class);
                }
            }
        }

        // Pass the request to other autoloaders (e.g. Swift)
    }

    /**
     * Search the namespaces for a matching entry
     *
     * @param string $class The class name
     *
     * @return string|null The full path including the namespace or null
     */
    protected static function findClass($class)
    {
        foreach (self::$namespaces as $namespace)
        {
            if (isset(self::$classes[$namespace . '\\' . $class]))
            {
                return $namespace . '\\' . $class;
            }
        }

        return null;
    }

    /**
     * Register the autoloader
     */
    public static function register()
    {
        spl_autoload_register('ClassLoader::load');
    }

    /**
     * Scan the module directories for config/autoload.php files and then
     * register the autoloader on the SPL stack
     */
    public static function scanAndRegister()
    {
        $strCacheDir = System::getContainer()->getParameter('kernel.cache_dir');

        // Try to load from cache
        if (file_exists($strCacheDir . '/contao/config/autoload.php'))
        {
            include $strCacheDir . '/contao/config/autoload.php';
        }
        else
        {
            try
            {
                $files = System::getContainer()->get('contao.resource_locator')->locate('config/autoload.php', null, false);
            }
            catch (\InvalidArgumentException $e)
            {
                $files = array();
            }

            foreach ($files as $file)
            {
                include $file;
            }
        }

        self::register();
    }
}

class_alias(ClassLoader::class, 'ClassLoader');
```

```php
namespace Contao;

class Config
{
    /**
     * Return all active modules as array
     *
     * @return array An array of active modules
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the container parameter "kernel.bundles" instead.
     */
    public function getActiveModules()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Config::getActiveModules()" has been deprecated and will no longer work in Contao 5.0. Use "kernel.bundles" instead.');

        return ModuleLoader::getActive();
    }
```

```php
namespace Contao;

abstract class Controller extends System
{
    /**
     * Replace insert tags with their values
     *
     * @param string  $strBuffer The text with the tags to be replaced
     * @param boolean $blnCache  If false, non-cacheable tags will be replaced
     *
     * @return string The text with the replaced tags
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use the InsertTagParser service instead.
     */
    public static function replaceInsertTags($strBuffer, $blnCache=true)
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "%s()" has been deprecated and will no longer work in Contao 5.0. Use the InsertTagParser service instead.', __METHOD__);

        $parser = System::getContainer()->get('contao.insert_tag.parser');

        if ($blnCache)
        {
            return $parser->replace((string) $strBuffer);
        }

        return $parser->replaceInline((string) $strBuffer);
    }

    /**
     * Compile the margin format definition based on an array of values
     *
     * @param array  $arrValues An array of four values and a unit
     * @param string $strType   Either "margin" or "padding"
     *
     * @return string The CSS markup
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     */
    public static function generateMargin($arrValues, $strType='margin')
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using Contao\Controller::generateMargin is deprecated since Contao 4.13 and will be removed in Contao 5.');

        // Initialize an empty array (see #5217)
        if (!\is_array($arrValues))
        {
            $arrValues = array('top'=>'', 'right'=>'', 'bottom'=>'', 'left'=>'', 'unit'=>'');
        }

        $top = $arrValues['top'];
        $right = $arrValues['right'];
        $bottom = $arrValues['bottom'];
        $left = $arrValues['left'];

        // Try to shorten the definition
        if ($top && $right && $bottom && $left)
        {
            if ($top == $right && $top == $bottom && $top == $left)
            {
                return $strType . ':' . $top . $arrValues['unit'] . ';';
            }

            if ($top == $bottom && $right == $left)
            {
                return $strType . ':' . $top . $arrValues['unit'] . ' ' . $left . $arrValues['unit'] . ';';
            }

            if ($top != $bottom && $right == $left)
            {
                return $strType . ':' . $top . $arrValues['unit'] . ' ' . $right . $arrValues['unit'] . ' ' . $bottom . $arrValues['unit'] . ';';
            }

            return $strType . ':' . $top . $arrValues['unit'] . ' ' . $right . $arrValues['unit'] . ' ' . $bottom . $arrValues['unit'] . ' ' . $left . $arrValues['unit'] . ';';
        }

        $return = array();
        $arrDir = compact('top', 'right', 'bottom', 'left');

        foreach ($arrDir as $k=>$v)
        {
            if ($v)
            {
                $return[] = $strType . '-' . $k . ':' . $v . $arrValues['unit'] . ';';
            }
        }

        return implode('', $return);
    }

    /**
     * Generate a front end URL
     *
     * @param array   $arrRow       An array of page parameters
     * @param string  $strParams    An optional string of URL parameters
     * @param string  $strForceLang Force a certain language
     * @param boolean $blnFixDomain Check the domain of the target page and append it if necessary
     *
     * @return string A URL that can be used in the front end
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.0.
     *             Use PageModel::getFrontendUrl() instead.
     */
    public static function generateFrontendUrl(array $arrRow, $strParams=null, $strForceLang=null, $blnFixDomain=false)
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\Controller::generateFrontendUrl()" has been deprecated and will no longer work in Contao 5.0. Use PageModel::getFrontendUrl() instead.');

        $page = new PageModel();
        $page->preventSaving(false);
        $page->setRow($arrRow);

        if (!isset($arrRow['rootId']))
        {
            $page->loadDetails();

            foreach (array('domain', 'rootLanguage', 'rootUseSSL') as $key)
            {
                if (isset($arrRow[$key]))
                {
                    $page->$key = $arrRow[$key];
                }
                else
                {
                    $arrRow[$key] = $page->$key;
                }
            }
        }

        // Set the language
        if ($strForceLang !== null)
        {
            $strForceLang = LocaleUtil::formatAsLocale($strForceLang);

            $page->language = $strForceLang;
            $page->rootLanguage = $strForceLang;

            if (System::getContainer()->getParameter('contao.legacy_routing'))
            {
                $page->urlPrefix = System::getContainer()->getParameter('contao.prepend_locale') ? $strForceLang : '';
            }
        }

        // Add the domain if it differs from the current one (see #3765 and #6927)
        if ($blnFixDomain)
        {
            $page->domain = $arrRow['domain'];
            $page->rootUseSSL = (bool) $arrRow['rootUseSSL'];
        }

        $objRouter = System::getContainer()->get('router');
        $strUrl = $objRouter->generate(PageRoute::PAGE_BASED_ROUTE_NAME, array(RouteObjectInterface::CONTENT_OBJECT => $page, 'parameters' => $strParams));

        // Remove path from absolute URLs
        if (0 === strncmp($strUrl, '/', 1) && 0 !== strncmp($strUrl, '//', 2))
        {
            $strUrl = substr($strUrl, \strlen(Environment::get('path')) + 1);
        }

        // Decode sprintf placeholders
        if (strpos($strParams, '%') !== false)
        {
            $arrMatches = array();
            preg_match_all('/%([sducoxXbgGeEfF])/', $strParams, $arrMatches);

            foreach (array_unique($arrMatches[1]) as $v)
            {
                $strUrl = str_replace('%25' . $v, '%' . $v, $strUrl);
            }
        }

        // HOOK: add custom logic
        if (isset($GLOBALS['TL_HOOKS']['generateFrontendUrl']) && \is_array($GLOBALS['TL_HOOKS']['generateFrontendUrl']))
        {
            foreach ($GLOBALS['TL_HOOKS']['generateFrontendUrl'] as $callback)
            {
                $strUrl = static::importStatic($callback[0])->{$callback[1]}($arrRow, $strParams, $strUrl);
            }
        }

        return $strUrl;
    }

    /**
     * Add an image to a template
     *
     * @param object          $template                The template object to add the image to
     * @param array           $rowData                 The element or module as array
     * @param integer|null    $maxWidth                An optional maximum width of the image
     * @param string|null     $lightboxGroupIdentifier An optional lightbox group identifier
     * @param FilesModel|null $filesModel              An optional files model
     *
     * @deprecated Deprecated since Contao 4.11, to be removed in Contao 5.0;
     *             use the Contao\CoreBundle\Image\Studio\FigureBuilder instead.
     */
    public static function addImageToTemplate($template, array $rowData, $maxWidth = null, $lightboxGroupIdentifier = null, FilesModel $filesModel = null): void
    {
        trigger_deprecation('contao/core-bundle', '4.11', 'Using Controller::addImageToTemplate() is deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\Image\Studio\FigureBuilder" class instead.');

        // Helper: Create metadata from the specified row data
        $createMetadataOverwriteFromRowData = static function (bool $interpretAsContentModel) use ($rowData)
        {
            if ($interpretAsContentModel)
            {
                // This will be null if "overwriteMeta" is not set
                return (new ContentModel())->setRow($rowData)->getOverwriteMetadata();
            }

            // Manually create metadata that always contains certain properties (BC)
            return new Metadata(array(
                Metadata::VALUE_ALT => $rowData['alt'] ?? '',
                Metadata::VALUE_TITLE => $rowData['imageTitle'] ?? '',
                Metadata::VALUE_URL => System::getContainer()->get('contao.insert_tag.parser')->replaceInline($rowData['imageUrl'] ?? ''),
                'linkTitle' => (string) ($rowData['linkTitle'] ?? ''),
            ));
        };

        // Helper: Create fallback template data with (mostly) empty fields (used if resource acquisition fails)
        $createFallBackTemplateData = static function () use ($filesModel, $rowData)
        {
            $templateData = array(
                'width' => null,
                'height' => null,
                'picture' => array(
                    'img' => array(
                        'src' => '',
                        'srcset' => '',
                    ),
                    'sources' => array(),
                    'alt' => '',
                    'title' => '',
                ),
                'singleSRC' => $rowData['singleSRC'],
                'src' => '',
                'linkTitle' => '',
                'margin' => '',
                'addImage' => true,
                'addBefore' => true,
                'fullsize' => false,
            );

            if (null !== $filesModel)
            {
                // Set empty metadata
                $templateData = array_replace_recursive(
                    $templateData,
                    array(
                        'alt' => '',
                        'caption' => '',
                        'imageTitle' => '',
                        'imageUrl' => '',
                    )
                );
            }

            return $templateData;
        };

        // Helper: Get size and margins and handle legacy $maxWidth option
        $getSizeAndMargin = static function () use ($rowData, $maxWidth)
        {
            $size = $rowData['size'] ?? null;
            $margin = StringUtil::deserialize($rowData['imagemargin'] ?? null);
            $maxWidth = (int) ($maxWidth ?? Config::get('maxImageWidth'));

            if (0 === $maxWidth)
            {
                return array($size, $margin);
            }

            trigger_deprecation('contao/core-bundle', '4.10', 'Using a maximum front end width has been deprecated and will no longer work in Contao 5.0. Remove the "maxImageWidth" configuration and use responsive images instead.');

            // Adjust margins if needed
            if ('px' === ($margin['unit'] ?? null))
            {
                $horizontalMargin = (int) ($margin['left'] ?? 0) + (int) ($margin['right'] ?? 0);

                if ($maxWidth - $horizontalMargin < 1)
                {
                    $margin['left'] = '';
                    $margin['right'] = '';
                }
                else
                {
                    $maxWidth -= $horizontalMargin;
                }
            }

            // Normalize size
            if ($size instanceof PictureConfiguration)
            {
                return array($size, $margin);
            }

            $size = StringUtil::deserialize($size);

            if (is_numeric($size))
            {
                $size = array(0, 0, (int) $size);
            }
            else
            {
                $size = (\is_array($size) ? $size : array()) + array(0, 0, 'crop');
                $size[0] = (int) $size[0];
                $size[1] = (int) $size[1];
            }

            // Adjust image size configuration if it exceeds the max width
            if ($size[0] > 0 && $size[1] > 0)
            {
                list($width, $height) = $size;
            }
            else
            {
                $container = System::getContainer();

                /** @var BoxInterface $originalSize */
                $originalSize = $container
                    ->get('contao.image.factory')
                    ->create($container->getParameter('kernel.project_dir') . '/' . $rowData['singleSRC'])
                    ->getDimensions()
                    ->getSize();

                $width = $originalSize->getWidth();
                $height = $originalSize->getHeight();
            }

            if ($width <= $maxWidth)
            {
                return array($size, $margin);
            }

            $size[0] = $maxWidth;
            $size[1] = (int) floor($maxWidth * ($height / $width));

            return array($size, $margin);
        };

        $figureBuilder = System::getContainer()->get('contao.image.studio')->createFigureBuilder();

        // Set image resource
        if (null !== $filesModel)
        {
            // Make sure model points to the same resource (BC)
            $filesModel = clone $filesModel;
            $filesModel->path = $rowData['singleSRC'];

            // Use source + metadata from files model (if not overwritten)
            $figureBuilder
                ->fromFilesModel($filesModel)
                ->setMetadata($createMetadataOverwriteFromRowData(true));

            $includeFullMetadata = true;
        }
        else
        {
            // Always ignore file metadata when building from path (BC)
            $figureBuilder
                ->fromPath($rowData['singleSRC'], false)
                ->setMetadata($createMetadataOverwriteFromRowData(false));

            $includeFullMetadata = false;
        }

        // Set size and lightbox configuration
        list($size, $margin) = $getSizeAndMargin();

        $lightboxSize = StringUtil::deserialize($rowData['lightboxSize'] ?? null) ?: null;

        $figure = $figureBuilder
            ->setSize($size)
            ->setLightboxGroupIdentifier($lightboxGroupIdentifier)
            ->setLightboxSize($lightboxSize)
            ->enableLightbox((bool) ($rowData['fullsize'] ?? false))
            ->buildIfResourceExists();

        if (null === $figure)
        {
            System::getContainer()->get('monolog.logger.contao.error')->error('Image "' . $rowData['singleSRC'] . '" could not be processed: ' . $figureBuilder->getLastException()->getMessage());

            // Fall back to apply a sparse data set instead of failing (BC)
            foreach ($createFallBackTemplateData() as $key => $value)
            {
                $template->$key = $value;
            }

            return;
        }

        // Build result and apply it to the template
        $figure->applyLegacyTemplateData($template, $margin, $rowData['floating'] ?? null, $includeFullMetadata);

        // Fall back to manually specified link title or empty string if not set (backwards compatibility)
        $template->linkTitle ??= StringUtil::specialchars($rowData['title'] ?? '');
    }

    /**
     * Set the static URL constants
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     */
    public static function setStaticUrls()
    {
        if (\defined('TL_FILES_URL'))
        {
            return;
        }

        if (\func_num_args() > 0)
        {
            trigger_deprecation('contao/core-bundle', '4.9', 'Using "Contao\Controller::setStaticUrls()" has been deprecated and will no longer work in Contao 5.0. Use the asset contexts instead.');

            if (!isset($GLOBALS['objPage']))
            {
                $GLOBALS['objPage'] = func_get_arg(0);
            }
        }

        \define('TL_ASSETS_URL', System::getContainer()->get('contao.assets.assets_context')->getStaticUrl());
        \define('TL_FILES_URL', System::getContainer()->get('contao.assets.files_context')->getStaticUrl());

        // Deprecated since Contao 4.0, to be removed in Contao 5.0
        \define('TL_SCRIPT_URL', TL_ASSETS_URL);
        \define('TL_PLUGINS_URL', TL_ASSETS_URL);
    }

    /**
     * Return the current theme as string
     *
     * @return string The name of the theme
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Backend::getTheme() instead.
     */
    public static function getTheme()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getTheme()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Backend::getTheme()" instead.');

        return Backend::getTheme();
    }

    /**
     * Return the back end themes as array
     *
     * @return array An array of available back end themes
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Backend::getThemes() instead.
     */
    public static function getBackendThemes()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getBackendThemes()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Backend::getThemes()" instead.');

        return Backend::getThemes();
    }

    /**
     * Get the details of a page including inherited parameters
     *
     * @param mixed $intId A page ID or a Model object
     *
     * @return PageModel The page model or null
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use PageModel::findWithDetails() or PageModel->loadDetails() instead.
     */
    public static function getPageDetails($intId)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getPageDetails()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\PageModel::findWithDetails()" or "Contao\PageModel->loadDetails()" instead.');

        if ($intId instanceof PageModel)
        {
            return $intId->loadDetails();
        }

        if ($intId instanceof Collection)
        {
            /** @var PageModel $objPage */
            $objPage = $intId->current();

            return $objPage->loadDetails();
        }

        if (\is_object($intId))
        {
            $strKey = __METHOD__ . '-' . $intId->id;

            // Try to load from cache
            if (Cache::has($strKey))
            {
                return Cache::get($strKey);
            }

            // Create a model from the database result
            $objPage = new PageModel();
            $objPage->setRow($intId->row());
            $objPage->loadDetails();

            Cache::set($strKey, $objPage);

            return $objPage;
        }

        // Invalid ID
        if ($intId < 1 || !\strlen($intId))
        {
            return null;
        }

        $strKey = __METHOD__ . '-' . $intId;

        // Try to load from cache
        if (Cache::has($strKey))
        {
            return Cache::get($strKey);
        }

        $objPage = PageModel::findWithDetails($intId);

        Cache::set($strKey, $objPage);

        return $objPage;
    }

    /**
     * Remove old XML files from the share directory
     *
     * @param boolean $blnReturn If true, only return the finds and don't delete
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Automator::purgeXmlFiles() instead.
     */
    protected function removeOldFeeds($blnReturn=false)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::removeOldFeeds()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Automator::purgeXmlFiles()" instead.');

        $this->import(Automator::class, 'Automator');
        $this->Automator->purgeXmlFiles($blnReturn);
    }

    /**
     * Return true if a class exists (tries to autoload the class)
     *
     * @param string $strClass The class name
     *
     * @return boolean True if the class exists
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the PHP function class_exists() instead.
     */
    protected function classFileExists($strClass)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::classFileExists()" has been deprecated and will no longer work in Contao 5.0. Use the PHP function "class_exists()" instead.');

        return class_exists($strClass);
    }

    /**
     * Restore basic entities
     *
     * @param string $strBuffer The string with the tags to be replaced
     *
     * @return string The string with the original entities
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use StringUtil::restoreBasicEntities() instead.
     */
    public static function restoreBasicEntities($strBuffer)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::restoreBasicEntities()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::restoreBasicEntities()" instead.');

        return StringUtil::restoreBasicEntities($strBuffer);
    }

    /**
     * Resize an image and crop it if necessary
     *
     * @param string  $image  The image path
     * @param integer $width  The target width
     * @param integer $height The target height
     * @param string  $mode   An optional resize mode
     *
     * @return boolean True if the image has been resized correctly
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Image::resize() instead.
     */
    protected function resizeImage($image, $width, $height, $mode='')
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::resizeImage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Image::resize()" instead.');

        return Image::resize($image, $width, $height, $mode);
    }

    /**
     * Resize an image and crop it if necessary
     *
     * @param string  $image  The image path
     * @param integer $width  The target width
     * @param integer $height The target height
     * @param string  $mode   An optional resize mode
     * @param string  $target An optional target to be replaced
     * @param boolean $force  Override existing target images
     *
     * @return string|null The image path or null
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Image::get() instead.
     */
    protected function getImage($image, $width, $height, $mode='', $target=null, $force=false)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getImage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Image::get()" instead.');

        return Image::get($image, $width, $height, $mode, $target, $force);
    }

    /**
     * Generate an image tag and return it as string
     *
     * @param string $src        The image path
     * @param string $alt        An optional alt attribute
     * @param string $attributes A string of other attributes
     *
     * @return string The image HTML tag
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Image::getHtml() instead.
     */
    public static function generateImage($src, $alt='', $attributes='')
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::generateImage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Image::getHtml()" instead.');

        return Image::getHtml($src, $alt, $attributes);
    }

    /**
     * Return the date picker string (see #3218)
     *
     * @return boolean
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Specify "datepicker"=>true in your DCA file instead.
     */
    protected function getDatePickerString()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getDatePickerString()" has been deprecated and will no longer work in Contao 5.0. Specify "\'datepicker\' => true" in your DCA file instead.');

        return true;
    }

    /**
     * Return the installed back end languages as array
     *
     * @return array An array of available back end languages
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the Contao\CoreBundle\Intl\Locales service instead.
     */
    protected function getBackendLanguages()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getBackendLanguages()" has been deprecated and will no longer work in Contao 5.0. Use the Contao\CoreBundle\Intl\Locales service instead.');

        return $this->getLanguages(true);
    }

    /**
     * Parse simple tokens that can be used to personalize newsletters
     *
     * @param string $strBuffer The text with the tokens to be replaced
     * @param array  $arrData   The replacement data as array
     *
     * @return string The text with the replaced tokens
     *
     * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0;
     *             Use the contao.string.simple_token_parser service instead.
     */
    protected function parseSimpleTokens($strBuffer, $arrData)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "Contao\Controller::parseSimpleTokens()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.string.simple_token_parser" service instead.');

        return System::getContainer()->get('contao.string.simple_token_parser')->parse($strBuffer, $arrData);
    }

    /**
     * Convert a DCA file configuration to be used with widgets
     *
     * @param array  $arrData  The field configuration array
     * @param string $strName  The field name in the form
     * @param mixed  $varValue The field value
     * @param string $strField The field name in the database
     * @param string $strTable The table name
     *
     * @return array An array that can be passed to a widget
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Widget::getAttributesFromDca() instead.
     */
    protected function prepareForWidget($arrData, $strName, $varValue=null, $strField='', $strTable='')
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::prepareForWidget()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Widget::getAttributesFromDca()" instead.');

        return Widget::getAttributesFromDca($arrData, $strName, $varValue, $strField, $strTable);
    }

    /**
     * Return the IDs of all child records of a particular record (see #2475)
     *
     * @param mixed   $arrParentIds An array of parent IDs
     * @param string  $strTable     The table name
     * @param boolean $blnSorting   True if the table has a sorting field
     * @param array   $arrReturn    The array to be returned
     * @param string  $strWhere     Additional WHERE condition
     *
     * @return array An array of child record IDs
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Database::getChildRecords() instead.
     */
    protected function getChildRecords($arrParentIds, $strTable, $blnSorting=false, $arrReturn=array(), $strWhere='')
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getChildRecords()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Database::getChildRecords()" instead.');

        return $this->Database->getChildRecords($arrParentIds, $strTable, $blnSorting, $arrReturn, $strWhere);
    }

    /**
     * Return the IDs of all parent records of a particular record
     *
     * @param integer $intId    The ID of the record
     * @param string  $strTable The table name
     *
     * @return array An array of parent record IDs
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Database::getParentRecords() instead.
     */
    protected function getParentRecords($intId, $strTable)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getParentRecords()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Database::getParentRecords()" instead.');

        return $this->Database->getParentRecords($intId, $strTable);
    }

    /**
     * Print an article as PDF and stream it to the browser
     *
     * @param ModuleModel $objArticle An article object
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use ModuleArticle->generatePdf() instead.
     */
    protected function printArticleAsPdf($objArticle)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::printArticleAsPdf()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\ModuleArticle->generatePdf()" instead.');

        $objArticle = new ModuleArticle($objArticle);
        $objArticle->generatePdf();
    }

    /**
     * Return all page sections as array
     *
     * @return array An array of active page sections
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             See https://github.com/contao/core/issues/4693.
     */
    public static function getPageSections()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::getPageSections()" has been deprecated and will no longer work in Contao 5.0.');

        return array('header', 'left', 'right', 'main', 'footer');
    }

    /**
     * Return a "selected" attribute if the option is selected
     *
     * @param string $strOption The option to check
     * @param mixed  $varValues One or more values to check against
     *
     * @return string The attribute or an empty string
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Widget::optionSelected() instead.
     */
    public static function optionSelected($strOption, $varValues)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::optionSelected()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Widget::optionSelected()" instead.');

        return Widget::optionSelected($strOption, $varValues);
    }

    /**
     * Return a "checked" attribute if the option is checked
     *
     * @param string $strOption The option to check
     * @param mixed  $varValues One or more values to check against
     *
     * @return string The attribute or an empty string
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Widget::optionChecked() instead.
     */
    public static function optionChecked($strOption, $varValues)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::optionChecked()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Widget::optionChecked()" instead.');

        return Widget::optionChecked($strOption, $varValues);
    }

    /**
     * Find a content element in the TL_CTE array and return the class name
     *
     * @param string $strName The content element name
     *
     * @return string The class name
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use ContentElement::findClass() instead.
     */
    public static function findContentElement($strName)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::findContentElement()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\ContentElement::findClass()" instead.');

        return ContentElement::findClass($strName);
    }

    /**
     * Find a front end module in the FE_MOD array and return the class name
     *
     * @param string $strName The front end module name
     *
     * @return string The class name
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Module::findClass() instead.
     */
    public static function findFrontendModule($strName)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using Contao\Controller::findFrontendModule() has been deprecated and will no longer work in Contao 5.0. Use Contao\Module::findClass() instead.');

        return Module::findClass($strName);
    }

    /**
     * Create an initial version of a record
     *
     * @param string  $strTable The table name
     * @param integer $intId    The ID of the element to be versioned
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Versions->initialize() instead.
     */
    protected function createInitialVersion($strTable, $intId)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::createInitialVersion()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Versions->initialize()" instead.');

        $objVersions = new Versions($strTable, $intId);
        $objVersions->initialize();
    }

    /**
     * Create a new version of a record
     *
     * @param string  $strTable The table name
     * @param integer $intId    The ID of the element to be versioned
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Versions->create() instead.
     */
    protected function createNewVersion($strTable, $intId)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Controller::createNewVersion()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Versions->create()" instead.');

        $objVersions = new Versions($strTable, $intId);
        $objVersions->create();
    }

```

```php
namespace Contao;

class Database
{
    /**
     * Execute a query and do not cache the result
     *
     * @param string $strQuery The query string
     *
     * @return Result The Result object
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Database::execute() instead.
     */
    public function executeUncached($strQuery)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Database::executeUncached()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Database::execute()" instead.');

        return $this->execute($strQuery);
    }

    /**
     * Always execute the query and add or replace an existing cache entry
     *
     * @param string $strQuery The query string
     *
     * @return Result The Result object
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Database::execute() instead.
     */
    public function executeCached($strQuery)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Database::executeCached()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Database::execute()" instead.');

        return $this->execute($strQuery);
    }
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '3.5', 'Using the "Contao\Encryption" class has been deprecated and will no longer work in Contao 5.0. Use the PHP password_* functions and a third-party library such as OpenSSL or phpseclib instead.');

/**
 * Encrypts and decrypts data
 *
 * The class can be used to encrypt and decrypt data based on the encryption
 * string that is set during the Contao installation.
 *
 * Usage:
 *
 *     $encrypted = Encryption::encrypt('Leo Feyer');
 *     $decrypted = Encryption::decrypt($encrypted);
 *
 * @deprecated Deprecated since Contao 3.5, to be removed in Contao 5.0.
 *             Use the PHP password_* functions and a third-party library such as OpenSSL or phpseclib instead.
 */
class Encryption
{
    /**
     * @deprecated Use a third-party library such as OpenSSL or phpseclib instead
     */
    public static function encrypt($varValue, $strKey=null)
    {
        throw new \BadMethodCallException('This method is not supported anymore, because the PHP mcrypt extension has been removed in PHP 7.2.');
    }

    /**
     * @deprecated Use a third-party library such as OpenSSL or phpseclib instead
     */
    public static function decrypt($varValue, $strKey=null)
    {
        throw new \BadMethodCallException('This method is not supported anymore, because the PHP mcrypt extension has been removed in PHP 7.2.');
    }
```

```php
namespace Contao;

class Environment
{
    /**
     * Return the operating system and the browser name and version
     *
     * @return object The agent information
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     */
    protected static function agent()
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "%s::get(\'agent\')" has been deprecated and will no longer work in Contao 5.0.', __CLASS__);

        $ua = static::get('httpUserAgent');

        $return = new \stdClass();
        $return->string = $ua;

        $os = 'unknown';
        $mobile = false;
        $browser = 'other';
        $shorty = '';
        $version = '';
        $engine = '';

        // Operating system
        foreach (Config::get('os') as $k=>$v)
        {
            if (stripos($ua, $k) !== false)
            {
                $os = $v['os'];
                $mobile = $v['mobile'];
                break;
            }
        }

        $return->os = $os;

        // Browser and version
        foreach (Config::get('browser') as $k=>$v)
        {
            if (stripos($ua, $k) !== false)
            {
                $browser = $v['browser'];
                $shorty  = $v['shorty'];
                $version = preg_replace($v['version'], '$1', $ua);
                $engine  = $v['engine'];
                break;
            }
        }

        $versions = explode('.', $version);
        $version  = $versions[0];

        $return->class = $os . ' ' . $browser . ' ' . $engine;

        // Add the version number if available
        if ($version)
        {
            $return->class .= ' ' . $shorty . $version;
        }

        // Android tablets are not mobile (see #4150 and #5869)
        if ($os == 'android' && $engine != 'presto' && stripos($ua, 'mobile') === false)
        {
            $mobile = false;
        }

        // Mark mobile devices
        if ($mobile)
        {
            $return->class .= ' mobile';
        }

        $return->browser  = $browser;
        $return->shorty   = $shorty;
        $return->version  = $version;
        $return->engine   = $engine;
        $return->versions = $versions;
        $return->mobile   = $mobile;

        return $return;
    }

    /**
     * Prevent direct instantiation (Singleton)
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Environment class is now static.
     */
    protected function __construct()
    {
    }

    /**
     * Prevent cloning of the object (Singleton)
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Environment class is now static.
     */
    final public function __clone()
    {
    }

    /**
     * Return an environment variable
     *
     * @param string $strKey The variable name
     *
     * @return string The variable value
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Environment::get() instead.
     */
    public function __get($strKey)
    {
        return static::get($strKey);
    }

    /**
     * Set an environment variable
     *
     * @param string $strKey   The variable name
     * @param mixed  $varValue The variable value
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Environment::set() instead.
     */
    public function __set($strKey, $varValue)
    {
        static::set($strKey, $varValue);
    }

    /**
     * Return the object instance (Singleton)
     *
     * @return Environment The object instance
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Environment class is now static.
     */
    public static function getInstance()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Environment::getInstance()" has been deprecated and will no longer work in Contao 5.0. The "Contao\Environment" class is now static.');

        if (static::$objInstance === null)
        {
            static::$objInstance = new static();
        }

        return static::$objInstance;
    }
```

```php
namespace Contao;

class Folder extends System
{
    /**
     * Purge the folder
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use $this->purge() instead.
     */
    public function clear()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Folder->clear()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Folder->purge()" instead.');

        $this->purge();
    }

    /**
     * Return the MD5 hash of the folder
     *
     * @return string The MD5 has
     *
     * @deprecated Use Dbafs::getFolderHash() instead
     */
    protected function getHash()
    {
        trigger_deprecation('contao/core-bundle', '4.4', 'Using "Contao\Folder::getHash()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Dbafs::getFolderHash()" instead.');

        $arrFiles = array();

        /** @var \SplFileInfo[] $it */
        $it = new \RecursiveIteratorIterator(
            new \RecursiveDirectoryIterator(
                $this->strRootDir . '/' . $this->strFolder,
                \FilesystemIterator::UNIX_PATHS|\FilesystemIterator::FOLLOW_SYMLINKS|\FilesystemIterator::SKIP_DOTS
            ),
            \RecursiveIteratorIterator::SELF_FIRST
        );

        foreach ($it as $i)
        {
            if (strncmp($i->getFilename(), '.', 1) !== 0)
            {
                $arrFiles[] = substr($i->getPathname(), \strlen($this->strRootDir . '/' . $this->strFolder . '/'));
            }
        }

        return md5(implode('-', $arrFiles));
    }

    /**
     * Check if the folder should be synchronized with the database
     *
     * @return bool True if the folder needs to be synchronized with the database
     *
     * @deprecated Use Dbafs::shouldBeSynchronized() instead
     */
    public function shouldBeSynchronized()
    {
        return Dbafs::shouldBeSynchronized($this->strFolder);
    }
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.3', 'Using the "Contao\GdImage" class has been deprecated and will no longer work in Contao 5.0. Use the Imagine library instead.');

/**
 * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
 *             Use the Imagine library instead.
 */
class GdImage
{
```

```php
namespace Contao;

class Image
{
    /**
     * Create a new object to handle an image
     *
     * @param File $file A file instance of the original image
     *
     * @throws \InvalidArgumentException If the file does not exist or cannot be processed
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
     *             Use the contao.image.factory service instead.
     */
    public function __construct(File $file)
    {
        trigger_deprecation('contao/core-bundle', '4.3', 'Using the "Contao\Image" class has been deprecated and will no longer work in Contao 5.0. Use the "contao.image.factory" service instead.');

        // Create deferred images (see #5873)
        $file->createIfDeferred();

        // Check whether the file exists
        if (!$file->exists())
        {
            $webDir = System::getContainer()->getParameter('contao.web_dir');

            // Handle public bundle resources
            if (file_exists($webDir . '/' . $file->path))
            {
                $file = new File(StringUtil::stripRootDir($webDir) . '/' . $file->path);
            }
            else
            {
                throw new \InvalidArgumentException('Image "' . $file->path . '" could not be found');
            }
        }

        $this->fileObj = $file;
        $arrAllowedTypes = System::getContainer()->getParameter('contao.image.valid_extensions');

        // Check the file type
        if (!\in_array($this->fileObj->extension, $arrAllowedTypes))
        {
            throw new \InvalidArgumentException('Image type "' . $this->fileObj->extension . '" was not allowed to be processed');
        }

        $this->strRootDir = System::getContainer()->getParameter('kernel.project_dir');
    }

    /**
     * Resize or crop an image and replace the original with the resized version
     *
     * @param string  $image  The image path
     * @param integer $width  The target width
     * @param integer $height The target height
     * @param string  $mode   The resize mode
     *
     * @return boolean True if the image could be resized successfully
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
     *             Use the contao.image.factory service instead.
     */
    public static function resize($image, $width, $height, $mode='')
    {
        trigger_deprecation('contao/core-bundle', '4.3', 'Using "Contao\Image::resize()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.image.factory" service instead.');

        return static::get($image, $width, $height, $mode, $image, true) ? true : false;
    }

    /**
     * Create an image instance from the given image path and size
     *
     * @param string|File          $image The image path or File instance
     * @param array|integer|string $size  The image size as array (width, height, resize mode) or a tl_image_size ID or a predefined image size key
     *
     * @return static The created image instance
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
     *             Use the contao.image.factory service instead.
     */
    public static function create($image, $size=null)
    {
        trigger_deprecation('contao/core-bundle', '4.3', 'Using "Contao\Image::create()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.image.factory" service instead.');

        if (\is_string($image))
        {
            $image = new File(rawurldecode($image));
        }

        $imageObj = new static($image);

        if (\is_array($size) && !empty($size[2]))
        {
            // tl_image_size ID as resize mode
            if (is_numeric($size[2]))
            {
                $size = (int) $size[2];
            }

            // Predefined image size as resize mode
            elseif (\is_string($size[2]) && $size[2][0] === '_')
            {
                $size = $size[2];
            }
        }

        if (\is_array($size))
        {
            $size += array(0, 0, 'crop');

            $imageObj
                ->setTargetWidth($size[0])
                ->setTargetHeight($size[1])
                ->setResizeMode($size[2])
            ;
        }

        // Load the image size from the database if $size is an ID or a predefined size
        elseif (($imageSize = self::getImageSizeConfig($size)) !== null)
        {
            $imageObj
                ->setTargetWidth($imageSize->width)
                ->setTargetHeight($imageSize->height)
                ->setResizeMode($imageSize->resizeMode)
                ->setZoomLevel($imageSize->zoom)
            ;
        }

        $fileRecord = FilesModel::findByPath($image->path);
        $currentSize = $image->imageViewSize;

        // Set the important part
        if ($fileRecord !== null && $fileRecord->importantPartWidth && $fileRecord->importantPartHeight)
        {
            $imageObj->setImportantPart(array
            (
                'x' => (int) ($fileRecord->importantPartX * $currentSize[0]),
                'y' => (int) ($fileRecord->importantPartY * $currentSize[1]),
                'width' => (int) ($fileRecord->importantPartWidth * $currentSize[0]),
                'height' => (int) ($fileRecord->importantPartHeight * $currentSize[1]),
            ));
        }

        return $imageObj;
    }

    /**
     * Resize an image and store the resized version in the image target folder
     *
     * @param string  $image  The image path
     * @param integer $width  The target width
     * @param integer $height The target height
     * @param string  $mode   The resize mode
     * @param string  $target An optional target path
     * @param boolean $force  Override existing target images
     *
     * @return string|null The path of the resized image or null
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
     *             Use the contao.image.factory service instead.
     */
    public static function get($image, $width, $height, $mode='', $target=null, $force=false)
    {
        trigger_deprecation('contao/core-bundle', '4.3', 'Using "Contao\Image::get()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.image.factory" service instead.');

        if (!$image)
        {
            return null;
        }

        try
        {
            $imageObj = static::create($image, array($width, $height, $mode));
            $imageObj->setTargetPath($target);
            $imageObj->setForceOverride($force);

            if ($path = $imageObj->executeResize()->getResizedPath())
            {
                return $path;
            }
        }
        catch (\Exception $e)
        {
            System::getContainer()->get('monolog.logger.contao.error')->error('Image "' . $image . '" could not be processed: ' . $e->getMessage());
        }

        return null;
    }

    /**
     * Convert sizes like 2em, 10cm or 12pt to pixels
     *
     * @param string $size The size string
     *
     * @return integer The pixel value
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
     *             Use the contao.image.factory service instead.
     */
    public static function getPixelValue($size)
    {
        trigger_deprecation('contao/core-bundle', '4.3', 'Using "Contao\Image::getPixelValue()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.image.factory" service instead.');

        $value = preg_replace('/[^0-9.-]+/', '', $size);
        $unit = preg_replace('/[^acehimnprtvwx%]/', '', $size);

        // Convert 16px = 1em = 2ex = 12pt = 1pc = 1/6in = 2.54/6cm = 25.4/6mm = 100%
        switch ($unit)
        {
            case '':
            case 'px':
                return (int) round($value);

            case 'pc':
            case 'em':
                return (int) round($value * 16);

            case 'ex':
                return (int) round($value * 16 / 2);

            case 'pt':
                return (int) round($value * 16 / 12);

            case 'in':
                return (int) round($value * 16 * 6);

            case 'cm':
                return (int) round($value * 16 / (2.54 / 6));

            case 'mm':
                return (int) round($value * 16 / (25.4 / 6));

            case '%':
                return (int) round($value * 16 / 100);
        }

        return 0;
    }
```

```php
namespace Contao;

class Input
{
    /**
     * Strip slashes
     *
     * @param mixed $varValue A string or array
     *
     * @return mixed The string or array without slashes
     *
     * @deprecated Deprecated since Contao 3.5, to be removed in Contao 5.
     *             Since get_magic_quotes_gpc() always returns false in PHP 5.4+, the method was never actually executed.
     */
    public static function stripSlashes($varValue)
    {
        return $varValue;
    }

    /**
     * Clean the keys of the request arrays
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Input class is now static.
     */
    protected function __construct()
    {
        static::initialize();
    }

    /**
     * Prevent cloning of the object (Singleton)
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Input class is now static.
     */
    final public function __clone()
    {
    }

    /**
     * Return the object instance (Singleton)
     *
     * @return Input The object instance
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Input class is now static.
     */
    public static function getInstance()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Input::getInstance()" has been deprecated and will no longer work in Contao 5.0. The "Contao\Input" class is now static.');

        if (static::$objInstance === null)
        {
            static::$objInstance = new static();
        }

        return static::$objInstance;
    }
```

```php
namespace Contao;

class InsertTags extends Controller
{

    /**
     * Recursively replace insert tags with their values
     *
     * @param string  $strBuffer The text with the tags to be replaced
     * @param boolean $blnCache  If false, non-cacheable tags will be replaced
     *
     * @return string The text with the replaced tags
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use the InsertTagParser service instead.
     */
    public function replace($strBuffer, $blnCache=true)
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "%s::%s()" has been deprecated and will no longer work in Contao 5.0. Use the InsertTagParser service instead.', __CLASS__, __METHOD__);

        return (string) $this->replaceInternal((string) $strBuffer, (bool) $blnCache);
    }
```

```php
namespace Contao;

/**
 * Loads modules based on their autoload.ini configuration
 *
 * The class reads the autoload.ini files of the available modules and returns
 * an array of active modules with their dependencies solved.
 *
 * Usage:
 *
 *     $arrModules = ModuleLoader::getActive();
 *     $arrModules = ModuleLoader::getDisabled();
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use the container parameter "kernel.bundles" instead.
 */
class ModuleLoader
{
    /**
     * Old module names
     * @var array
     */
    private static $legacy = array
    (
        'ContaoCoreBundle'       => 'core',
        'ContaoCalendarBundle'   => 'calendar',
        'ContaoCommentsBundle'   => 'comments',
        'ContaoFaqBundle'        => 'faq',
        'ContaoListingBundle'    => 'listing',
        'ContaoNewsBundle'       => 'news',
        'ContaoNewsletterBundle' => 'newsletter'
    );

    /**
     * Return the active modules as array
     *
     * @return array An array of active modules
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.
     */
    public static function getActive()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\ModuleLoader::getActive()" has been deprecated and will no longer work in Contao 5.0.');

        $bundles = array_keys(System::getContainer()->getParameter('kernel.bundles'));

        foreach (static::$legacy as $bundleName => $module)
        {
            if (\in_array($bundleName, $bundles))
            {
                $bundles[] = $module;
            }
        }

        return $bundles;
    }

    /**
     * Return the disabled modules as array
     *
     * @return array An array of disabled modules
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.
     */
    public static function getDisabled()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\ModuleLoader::getDisabled()" has been deprecated and will no longer work in Contao 5.0.');

        return array();
    }
}

class_alias(ModuleLoader::class, 'ModuleLoader');

```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.3', 'Using the "Contao\Picture" class has been deprecated and will no longer work in Contao 5.0. Use the "contao.image.picture_factory" service instead.');

/**
 * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.0.
 *             Use the contao.image.picture_factory service instead.
 */
class Picture
{
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.0', 'Using the "Contao\RequestToken" class has been deprecated and will no longer work in Contao 5.0. Use the Symfony CSRF service via the container instead.');

/**
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use the Symfony CSRF service via the container instead.
 */
class RequestToken
{
```

```php
namespace Contao;

class Search
{
    /**
     * Search the index and return the result object
     *
     * @param string  $strKeywords  The keyword string
     * @param boolean $blnOrSearch  If true, the result can contain any keyword
     * @param array   $arrPid       An optional array of page IDs to limit the result to
     * @param integer $intRows      An optional maximum number of result rows
     * @param integer $intOffset    An optional result offset
     * @param boolean $blnFuzzy     If true, the search will be fuzzy
     * @param integer $intMinlength Ignore keywords deceeding the minimum length
     *
     * @return Result The database result object
     *
     * @throws \Exception If the cleaned keyword string is empty
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.
     *             Use the Search::query() method instead.
     */
    public static function searchFor($strKeywords, $blnOrSearch=false, $arrPid=array(), $intRows=0, $intOffset=0, $blnFuzzy=false, $intMinlength=0)
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using "%s()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Search::query()" instead.', __METHOD__);

        $objSearchResult = static::query((string) $strKeywords, (bool) $blnOrSearch, \is_array($arrPid) ? $arrPid : array(), (bool) $blnFuzzy, (int) $intMinlength);

        return new Result($objSearchResult->getResults($intRows ?: PHP_INT_MAX, $intOffset), 'SELECT * FROM tl_search');
    }

    /**
     * Prevent cloning of the object (Singleton)
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Search class is now static.
     */
    final public function __clone()
    {
    }

    /**
     * Return the object instance (Singleton)
     *
     * @return Search The object instance
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             The Search class is now static.
     */
    public static function getInstance()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Search::getInstance()" has been deprecated and will no longer work in Contao 5.0. The "Contao\Search" class is now static.');

        if (static::$objInstance === null)
        {
            static::$objInstance = new static();
        }

        return static::$objInstance;
    }
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.0', 'Using the "Contao\Session" class has been deprecated and will no longer work in Contao 5.0. Use the session service instead.');

/**
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 *             Use the session service instead.
 */
class Session
{
```

```php
namespace Contao;

use Symfony\Component\Filesystem\Path;

class StringUtil
{
    /**
     * Convert a string to XHTML
     *
     * @param string $strString The HTML5 string
     *
     * @return string The XHTML string
     *
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0
     */
    public static function toXhtml($strString)
    {
        trigger_deprecation('contao/core-bundle', '4.9', 'The "StringUtil::toXhtml()" method has been deprecated and will no longer work in Contao 5.0.');

        $arrPregReplace = array
        (
            '/<(br|hr|img)([^>]*)>/i' => '<$1$2 />', // Close stand-alone tags
            '/ border="[^"]*"/'       => ''          // Remove deprecated attributes
        );

        $arrStrReplace = array
        (
            '/ />'             => ' />',        // Fix incorrectly closed tags
            '<b>'              => '<strong>',   // Replace <b> with <strong>
            '</b>'             => '</strong>',
            '<i>'              => '<em>',       // Replace <i> with <em>
            '</i>'             => '</em>',
            '<u>'              => '<span style="text-decoration:underline">',
            '</u>'             => '</span>',
            ' target="_self"'  => '',
            ' target="_blank"' => ' onclick="return !window.open(this.href)"'
        );

        $strString = preg_replace(array_keys($arrPregReplace), $arrPregReplace, $strString);
        $strString = str_ireplace(array_keys($arrStrReplace), $arrStrReplace, $strString);

        return $strString;
    }

    /**
     * Convert a string to HTML5
     *
     * @param string $strString The XHTML string
     *
     * @return string The HTML5 string
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0
     */
    public static function toHtml5($strString)
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'The "StringUtil::toHtml5()" method has been deprecated and will no longer work in Contao 5.0.');

        $arrPregReplace = array
        (
            '/<(br|hr|img)([^>]*) \/>/i'                  => '<$1$2>',             // Close stand-alone tags
            '/ (cellpadding|cellspacing|border)="[^"]*"/' => '',                   // Remove deprecated attributes
            '/ rel="lightbox(\[([^\]]+)\])?"/'            => ' data-lightbox="$2"' // see #4073
        );

        $arrStrReplace = array
        (
            '<u>'                                              => '<span style="text-decoration:underline">',
            '</u>'                                             => '</span>',
            ' target="_self"'                                  => '',
            ' onclick="window.open(this.href); return false"'  => ' target="_blank"',
            ' onclick="window.open(this.href);return false"'   => ' target="_blank"',
            ' onclick="window.open(this.href); return false;"' => ' target="_blank"'
        );

        $strString = preg_replace(array_keys($arrPregReplace), $arrPregReplace, $strString);
        $strString = str_ireplace(array_keys($arrStrReplace), $arrStrReplace, $strString);

        return $strString;
    }

    /**
     * Parse simple tokens
     *
     * @param string $strString    The string to be parsed
     * @param array  $arrData      The replacement data
     * @param array  $blnAllowHtml Whether HTML should be decoded inside conditions
     *
     * @return string The converted string
     *
     * @throws \RuntimeException         If $strString cannot be parsed
     * @throws \InvalidArgumentException If there are incorrectly formatted if-tags
     *
     * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.
     *             Use the contao.string.simple_token_parser service instead.
     */
    public static function parseSimpleTokens($strString, $arrData, $blnAllowHtml = true)
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using "Contao\StringUtil::parseSimpleTokens()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.string.simple_token_parser" service instead.');

        return System::getContainer()->get('contao.string.simple_token_parser')->parse($strString, $arrData, $blnAllowHtml);
    }

    /**
     * Convert an input-encoded string to plain text UTF-8
     *
     * Strips or replaces insert tags, strips HTML tags, decodes entities, escapes insert tag braces.
     *
     * @param bool $blnRemoveInsertTags True to remove insert tags instead of replacing them
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5;
     *             use the Contao\CoreBundle\String\HtmlDecoder service instead
     */
    public static function inputEncodedToPlainText(string $strValue, bool $blnRemoveInsertTags = false): string
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "StringUtil::inputEncodedToPlainText()" has been deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\String\HtmlDecoder" service instead.');

        return System::getContainer()->get('contao.string.html_decoder')->inputEncodedToPlainText($strValue, $blnRemoveInsertTags);
    }

    /**
     * Convert an HTML string to plain text with normalized white space
     *
     * It handles all Contao input encoding specifics like insert tags, basic
     * entities and encoded entities and is meant to be used with content from
     * fields that have the allowHtml flag enabled.
     *
     * @param bool $blnRemoveInsertTags True to remove insert tags instead of replacing them
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5;
     *             use the Contao\CoreBundle\String\HtmlDecoder service instead
     */
    public static function htmlToPlainText(string $strValue, bool $blnRemoveInsertTags = false): string
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "StringUtil::htmlToPlainText()" has been deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\String\HtmlDecoder" service instead.');

        return System::getContainer()->get('contao.string.html_decoder')->htmlToPlainText($strValue, $blnRemoveInsertTags);
    }
```

```php
namespace Contao;

/**
 * @property BackendTemplate|FrontendTemplate $Template    The template object (TODO: remove this line in Contao 5.0)
 */
abstract class System
{
    /**
     * Cache
     * @var array
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     */
    protected $arrCache = array();

        /**
     * Add a log entry to the database
     *
     * @param string $strText     The log message
     * @param string $strFunction The function name
     * @param string $strCategory The category name
     *
     * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.
     *             Use the logger service with your context or any of the predefined monolog.logger.contao services instead.
     */
    public static function log($strText, $strFunction, $strCategory)
    {
        trigger_deprecation('contao/core-bundle', '4.2', 'Using "Contao\System::log()" has been deprecated and will no longer work in Contao 5.0. Use the "logger" service or any of the predefined "monolog.logger.contao" services instead.');

        $level = 'ERROR' === $strCategory ? LogLevel::ERROR : LogLevel::INFO;
        $logger = static::getContainer()->get('monolog.logger.contao');

        $logger->log($level, $strText, array('contao' => new ContaoContext($strFunction, $strCategory)));
    }

    /**
     * Return the countries as array
     *
     * @return array An array of country names
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5;
     *             use the Contao\CoreBundle\Intl\Countries service instead
     */
    public static function getCountries()
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using the %s method has been deprecated and will no longer work in Contao 5.0. Use the "contao.intl.countries" service instead.', __METHOD__);

        $arrCountries = self::getContainer()->get('contao.intl.countries')->getCountries();

        return array_combine(array_map('strtolower', array_keys($arrCountries)), $arrCountries);
    }

    /**
     * Return the available languages as array
     *
     * @param boolean $blnInstalledOnly If true, return only installed languages
     *
     * @return array An array of languages
     *
     * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5;
     *             use the Contao\CoreBundle\Intl\Locales service instead
     */
    public static function getLanguages($blnInstalledOnly=false)
    {
        trigger_deprecation('contao/core-bundle', '4.12', 'Using the %s method has been deprecated and will no longer work in Contao 5.0. Use the "contao.intl.locales" service instead.', __METHOD__);

        if ($blnInstalledOnly)
        {
            return self::getContainer()->get('contao.intl.locales')->getEnabledLocales(null, true);
        }

        return self::getContainer()->get('contao.intl.locales')->getLocales(null, true);
    }

    /**
     * Return all image sizes as array
     *
     * @return array The available image sizes
     *
     * @deprecated Deprecated since Contao 4.1, to be removed in Contao 5.
     *             Use the contao.image.sizes service instead.
     */
    public static function getImageSizes()
    {
        trigger_deprecation('contao/core-bundle', '4.1', 'Using "Contao\System::getImageSizes()" has been deprecated and will no longer work in Contao 5.0. Use the "contao.image.sizes" service instead.');

        return static::getContainer()->get('contao.image.sizes')->getAllOptions();
    }

    /**
     * Return the session hash
     *
     * @param string $strCookie The cookie name
     *
     * @return string The session hash
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony authentication instead.
     */
    public static function getSessionHash($strCookie)
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\System::getSessionHash()" has been deprecated and will no longer work in Contao 5.0. Use Symfony authentication instead.');

        $session = static::getContainer()->get('session');

        if (!$session->isStarted())
        {
            $session->start();
        }

        return sha1($session->getId() . $strCookie);
    }

    /**
     * Read the contents of a PHP file, stripping the opening and closing PHP tags
     *
     * @param string $strName The name of the PHP file
     *
     * @return string The PHP code without the PHP tags
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the Contao\CoreBundle\Config\Loader\PhpFileLoader class instead.
     */
    protected static function readPhpFileWithoutTags($strName)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::readPhpFileWithoutTags()" has been deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\Config\Loader\PhpFileLoader" class instead.');

        $projectDir = self::getContainer()->getParameter('kernel.project_dir');

        // Convert to absolute path
        if (strpos($strName, $projectDir . '/') === false)
        {
            $strName = $projectDir . '/' . $strName;
        }

        $loader = new PhpFileLoader();

        return $loader->load($strName);
    }

    /**
     * Convert an .xlf file into a PHP language file
     *
     * @param string  $strName     The name of the .xlf file
     * @param string  $strLanguage The language code
     * @param boolean $blnLoad     Add the labels to the global language array
     *
     * @return string The PHP code
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use the Contao\CoreBundle\Config\Loader\XliffFileLoader class instead.
     */
    public static function convertXlfToPhp($strName, $strLanguage, $blnLoad=false)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::convertXlfToPhp()" has been deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\Config\Loader\XliffFileLoader" class instead.');

        $projectDir = self::getContainer()->getParameter('kernel.project_dir');

        // Convert to absolute path
        if (strpos($strName, $projectDir . '/') === false)
        {
            $strName = $projectDir . '/' . $strName;
        }

        $loader = new XliffFileLoader(static::getContainer()->getParameter('kernel.project_dir'), $blnLoad);

        return $loader->load($strName, $strLanguage);
    }

    /**
     * Parse a date format string and translate textual representations
     *
     * @param string  $strFormat The date format string
     * @param integer $intTstamp An optional timestamp
     *
     * @return string The textual representation of the date
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Date::parse() instead.
     */
    public static function parseDate($strFormat, $intTstamp=null)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::parseDate()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Date::parse()" instead.');

        return Date::parse($strFormat, $intTstamp);
    }

    /**
     * Add a request string to the current URL
     *
     * @param string $strRequest The string to be added
     *
     * @return string The new URL
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Controller::addToUrl() instead.
     */
    public static function addToUrl($strRequest)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::addToUrl()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Controller::addToUrl()" instead.');

        return Controller::addToUrl($strRequest);
    }

    /**
     * Reload the current page
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Controller::reload() instead.
     */
    public static function reload()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::reload()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Controller::reload()" instead.');

        Controller::reload();
    }

    /**
     * Redirect to another page
     *
     * @param string  $strLocation The target URL
     * @param integer $intStatus   The HTTP status code (defaults to 303)
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Controller::redirect() instead.
     */
    public static function redirect($strLocation, $intStatus=303)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::redirect()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Controller::redirect()" instead.');

        Controller::redirect($strLocation, $intStatus);
    }

    /**
     * Add an error message
     *
     * @param string $strMessage The error message
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::addError() instead.
     */
    protected function addErrorMessage($strMessage)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::addErrorMessage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::addError()" instead.');

        Message::addError($strMessage);
    }

    /**
     * Add a confirmation message
     *
     * @param string $strMessage The confirmation
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::addConfirmation() instead.
     */
    protected function addConfirmationMessage($strMessage)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::addConfirmationMessage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::addConfirmation()" instead.');

        Message::addConfirmation($strMessage);
    }

    /**
     * Add a new message
     *
     * @param string $strMessage The new message
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::addNew() instead.
     */
    protected function addNewMessage($strMessage)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::addNewMessage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::addNew()" instead.');

        Message::addNew($strMessage);
    }

    /**
     * Add an info message
     *
     * @param string $strMessage The info message
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::addInfo() instead.
     */
    protected function addInfoMessage($strMessage)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::addInfoMessage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::addInfo()" instead.');

        Message::addInfo($strMessage);
    }

    /**
     * Add an unformatted message
     *
     * @param string $strMessage The unformatted message
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::addRaw() instead.
     */
    protected function addRawMessage($strMessage)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::addRawMessage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::addRaw()" instead.');

        Message::addRaw($strMessage);
    }

    /**
     * Add a message
     *
     * @param string $strMessage The message
     * @param string $strType    The message type
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::add() instead.
     */
    protected function addMessage($strMessage, $strType)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::addMessage()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::add()" instead.');

        Message::add($strMessage, $strType);
    }

    /**
     * Return all messages as HTML
     *
     * @param string $strScope An optional message scope
     *
     * @return string The messages HTML markup
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::generate() instead.
     */
    protected function getMessages($strScope=null)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::getMessages()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::generate()" instead.');

        return Message::generate($strScope ?? TL_MODE);
    }

    /**
     * Reset the message system
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::reset() instead.
     */
    protected function resetMessages()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::resetMessages()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::reset()" instead.');

        Message::reset();
    }

    /**
     * Return all available message types
     *
     * @return array An array of message types
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Message::getTypes() instead.
     */
    protected function getMessageTypes()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::getMessageTypes()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Message::getTypes()" instead.');

        return Message::getTypes();
    }

    /**
     * Encode an internationalized domain name
     *
     * @param string $strDomain The domain name
     *
     * @return string The encoded domain name
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Idna::encode() instead.
     */
    protected function idnaEncode($strDomain)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::idnaEncode()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Idna::encode()" instead.');

        return Idna::encode($strDomain);
    }

    /**
     * Decode an internationalized domain name
     *
     * @param string $strDomain The domain name
     *
     * @return string The decoded domain name
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Idna::decode() instead.
     */
    protected function idnaDecode($strDomain)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::idnaDecode()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Idna::decode()" instead.');

        return Idna::decode($strDomain);
    }

    /**
     * Encode the domain in an e-mail address
     *
     * @param string $strEmail The e-mail address
     *
     * @return string The encoded e-mail address
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Idna::encodeEmail() instead.
     */
    protected function idnaEncodeEmail($strEmail)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::idnaEncodeEmail()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Idna::encodeEmail()" instead.');

        return Idna::encodeEmail($strEmail);
    }

    /**
     * Encode the domain in a URL
     *
     * @param string $strUrl The URL
     *
     * @return string The encoded URL
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Idna::encodeUrl() instead.
     */
    protected function idnaEncodeUrl($strUrl)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::idnaEncodeUrl()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Idna::encodeUrl()" instead.');

        return Idna::encodeUrl($strUrl);
    }

    /**
     * Validate an e-mail address
     *
     * @param string $strEmail The e-mail address
     *
     * @return boolean True if it is a valid e-mail address
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Validator::isEmail() instead.
     */
    protected function isValidEmailAddress($strEmail)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::isValidEmailAddress()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Validator::isEmail()" instead.');

        return Validator::isEmail($strEmail);
    }

    /**
     * Split a friendly-name e-mail address and return name and e-mail as array
     *
     * @param string $strEmail A friendly-name e-mail address
     *
     * @return array An array with name and e-mail address
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use StringUtil::splitFriendlyEmail() instead.
     */
    public static function splitFriendlyName($strEmail)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::splitFriendlyName()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\StringUtil::splitFriendlyEmail()" instead.');

        return StringUtil::splitFriendlyEmail($strEmail);
    }

    /**
     * Return the request string without the script name
     *
     * @param boolean $blnAmpersand If true, ampersands will be encoded
     *
     * @return string The request string
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Environment::get("indexFreeRequest") instead.
     */
    public static function getIndexFreeRequest($blnAmpersand=true)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::getIndexFreeRequest()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Environment::get(\'indexFreeRequest\')" instead.');

        return StringUtil::ampersand(Environment::get('indexFreeRequest'), $blnAmpersand);
    }

    /**
     * Compile a Model class name from a table name (e.g. tl_form_field becomes FormFieldModel)
     *
     * @param string $strTable The table name
     *
     * @return string The model class name
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Model::getClassFromTable() instead.
     */
    public static function getModelClassFromTable($strTable)
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::getModelClassFromTable()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Model::getClassFromTable()" instead.');

        return Model::getClassFromTable($strTable);
    }

    /**
     * Enable a back end module
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Composer to add or remove modules.
     */
    public static function enableModule()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::enableModule()" has been deprecated and will no longer work in Contao 5.0. Use Composer to add or remove modules.');
    }

    /**
     * Disable a back end module
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Composer to add or remove modules.
     */
    public static function disableModule()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\System::disableModule()" has been deprecated and will no longer work in Contao 5.0. Use Composer to add or remove modules.');
    }
```

```php
namespace Contao;

abstract class Template extends Controller
{
    /**
     * Print all template variables to the screen using print_r
     *
     * @deprecated Deprecated since Contao 4.3, to be removed in Contao 5.
     *             Use Template::dumpTemplateVars() instead.
     */
    public function showTemplateVars()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Template::showTemplateVars()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Template::dumpTemplateVars()" instead.');

        $this->dumpTemplateVars();
    }

    /**
     * Parse the template file and print it to the screen
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     *             Use Template::getResponse() instead.
     */
    public function output()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Template::output()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Template::getResponse()" instead.');

        $this->compile();

        header('Content-Type: ' . $this->strContentType . '; charset=' . System::getContainer()->getParameter('kernel.charset'));

        echo $this->strBuffer;
    }

    /**
     * Return the debug bar string
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     */
    protected function getDebugBar()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Template::getDebugBar()" has been deprecated and will no longer work in Contao 5.0.');
    }

    /**
     * Flush the output buffers
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     */
    public function flushAllData()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Template::flushAllData()" has been deprecated and will no longer work in Contao 5.0.');

        if (\function_exists('fastcgi_finish_request'))
        {
            fastcgi_finish_request();
        }
        elseif (\PHP_SAPI !== 'cli')
        {
            $status = ob_get_status(true);
            $level = \count($status);

            while ($level-- > 0 && (!empty($status[$level]['del']) || (isset($status[$level]['flags']) && ($status[$level]['flags'] & PHP_OUTPUT_HANDLER_REMOVABLE) && ($status[$level]['flags'] & PHP_OUTPUT_HANDLER_FLUSHABLE))))
            {
                ob_end_flush();
            }

            flush();
        }
    }
```

```php
namespace Contao;

abstract class User extends System implements UserInterface, EquatableInterface, PasswordAuthenticatedUserInterface, \Serializable
{
    /**
     * Authenticate a user
     *
     * @return boolean True if the user could be authenticated
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    public function authenticate()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\User::authenticate()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        return false;
    }

    /**
     * Try to login the current user
     *
     * @return boolean True if the user could be logged in
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    public function login()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\User::login()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        return false;
    }

    /**
     * Check the account status and return true if it is active
     *
     * @return boolean True if the account is active
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony security instead.
     */
    protected function checkAccountStatus()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\User::checkAccountStatus()" has been deprecated and will no longer work in Contao 5.0. Use Symfony security instead.');

        try
        {
            $userChecker = System::getContainer()->get('contao.security.user_checker');
            $userChecker->checkPreAuth($this);
            $userChecker->checkPostAuth($this);
        }
        catch (AuthenticationException $exception)
        {
            return false;
        }

        return true;
    }

    /**
     * Regenerate the session ID
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony authentication instead.
     */
    protected function regenerateSessionId()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\User::regenerateSessionId()" has been deprecated and will no longer work in Contao 5.0. Use Symfony authentication instead.');

        $container = System::getContainer();
        $strategy = $container->getParameter('security.authentication.session_strategy.strategy');

        // Regenerate the session ID to harden against session fixation attacks
        switch ($strategy)
        {
            case SessionAuthenticationStrategy::NONE:
                break;

            case SessionAuthenticationStrategy::MIGRATE:
                $container->get('session')->migrate(); // do not destroy the old session
                break;

            case SessionAuthenticationStrategy::INVALIDATE:
                $container->get('session')->invalidate();
                break;

            default:
                throw new \RuntimeException(sprintf('Invalid session authentication strategy "%s"', $strategy));
        }
    }

    /**
     * Generate a session
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony authentication instead.
     */
    protected function generateSession()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\User::generateSession()" has been deprecated and will no longer work in Contao 5.0. Use Symfony authentication instead.');
    }

    /**
     * Remove the authentication cookie and destroy the current session
     *
     * @return never
     *
     * @throws RedirectResponseException
     *
     * @deprecated Deprecated since Contao 4.5, to be removed in Contao 5.0.
     *             Use Symfony authentication instead.
     */
    public function logout()
    {
        trigger_deprecation('contao/core-bundle', '4.5', 'Using "Contao\User::logout()" has been deprecated and will no longer work in Contao 5.0. Use Symfony authentication instead.');

        throw new RedirectResponseException(System::getContainer()->get('security.logout_url_generator')->getLogoutUrl());
    }

    /**
     * @return User
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use Contao\User::loadUserByIdentifier() instead.
     */
    public static function loadUserByUsername($username)
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "Contao\User::loadUserByUsername()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\User::loadUserByIdentifier()" instead.');

        return self::loadUserByIdentifier($username);
    }

    /**
     * {@inheritdoc}
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     *             Use Contao\User::getUserIdentifier() instead.
     */
    public function getUsername()
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "Contao\User::getUsername()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\User::getUserIdentifier()" instead.');

        return $this->getUserIdentifier();
    }

    /**
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0.
     */
    public function serialize()
    {
        return serialize($this->__serialize());
    }

    /**
     * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0.
     */
    public function unserialize($data)
    {
        $this->__unserialize(unserialize($data, array('allowed_classes'=>false)));
    }

    /**
     * Trigger the importUser hook
     *
     * @param $username
     * @param $password
     * @param $strTable
     *
     * @return bool|static
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
     */
    public static function triggerImportUserHook($username, $password, $strTable)
    {
        $self = new static();

        if (empty($GLOBALS['TL_HOOKS']['importUser']) || !\is_array($GLOBALS['TL_HOOKS']['importUser']))
        {
            return false;
        }

        trigger_deprecation('contao/core-bundle', '4.13', 'Using the "importUser" hook has been deprecated and will no longer work in Contao 5.0.');

        foreach ($GLOBALS['TL_HOOKS']['importUser'] as $callback)
        {
            $self->import($callback[0], 'objImport', true);
            $blnLoaded = $self->objImport->{$callback[1]}($username, $password, $strTable);

            // Load successfull
            if ($blnLoaded === true)
            {
                return true;
            }
        }

        return false;
    }
```

```php
namespace Contao;

abstract class Widget extends Controller
{
    /**
     * Generate a submit button
     *
     * @return string The submit button markup
     *
     * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
     */
    protected function addSubmit()
    {
        trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Widget::addSubmit()" has been deprecated and will no longer work in Contao 5.0.');

        return '';
    }
```

```php
namespace Contao\Database;

class Installer extends Controller
{
/**
	 * Generate an HTML form with queries and return it as string
	 *
	 * @return string The form HTML markup
	 *
	 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
	 */
	public function generateSqlForm()
	{
		trigger_deprecation('contao/core-bundle', '4.0', 'Using the "Contao\Installer::generateSqlForm()" method has been deprecated and will no longer work in Contao 5.0.');

		$count = 0;
		$return = '';
		$sql_command = $this->compileCommands();

		if (empty($sql_command))
		{
			return '';
		}

		$_SESSION['sql_commands'] = array();

		$arrOperations = array
		(
			'CREATE'        => $GLOBALS['TL_LANG']['tl_install']['CREATE'],
			'ALTER_ADD'     => $GLOBALS['TL_LANG']['tl_install']['ALTER_ADD'],
			'ALTER_CHANGE'  => $GLOBALS['TL_LANG']['tl_install']['ALTER_CHANGE'],
			'ALTER_DROP'    => $GLOBALS['TL_LANG']['tl_install']['ALTER_DROP'],
			'DROP'          => $GLOBALS['TL_LANG']['tl_install']['DROP']
		);

		foreach ($arrOperations as $command=>$label)
		{
			if (\is_array($sql_command[$command]))
			{
				// Headline
				$return .= '
    <tr>
      <td colspan="2" class="tl_col_0">' . $label . '</td>
    </tr>';

				// Check all
				$return .= '
    <tr>
      <td class="tl_col_1"><input type="checkbox" id="check_all_' . $count . '" class="tl_checkbox" onclick="Backend.toggleCheckboxElements(this, \'' . strtolower($command) . '\')"></td>
      <td class="tl_col_2"><label for="check_all_' . $count . '" style="color:#a6a6a6"><em>' . $GLOBALS['TL_LANG']['MSC']['selectAll'] . '</em></label></td>
    </tr>';

				// Fields
				foreach ($sql_command[$command] as $vv)
				{
					$key = md5($vv);
					$_SESSION['sql_commands'][$key] = $vv;

					$return .= '
    <tr>
      <td class="tl_col_1"><input type="checkbox" name="sql[]" id="sql_' . $count . '" class="tl_checkbox ' . strtolower($command) . '" value="' . $key . '"' . ((stripos($command, 'DROP') === false) ? ' checked="checked"' : '') . '></td>
      <td class="tl_col_2"><pre><label for="sql_' . $count++ . '">' . $vv . '</label></pre></td>
    </tr>';
				}
			}
		}

		return '
<div id="sql_wrapper">
  <table id="sql_table">' . $return . '
  </table>
</div>';
	}
```

```php
namespace Contao\Database;

class Statement
{
	/**
	 * Replace the wildcards in the query string
	 *
	 * @param array $arrValues The values array
	 *
	 * @throws \Exception If $arrValues has too few values to replace the wildcards in the query string
	 *
	 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
	 */
	protected function replaceWildcards($arrValues)
	{
		trigger_deprecation('contao/core-bundle', '4.13', 'Using "%s()" has been deprecated and will no longer work in Contao 5.0.', __METHOD__);

		$arrValues = $this->escapeParams($arrValues);
		$this->strQuery = preg_replace('/(?<!%)%([^bcdufosxX%])/', '%%$1', $this->strQuery);

		// Replace wildcards
		if (!$this->strQuery = @vsprintf($this->strQuery, $arrValues))
		{
			throw new \Exception('Too few arguments to build the query string');
		}
	}

	/**
	 * Escape the values and serialize objects and arrays
	 *
	 * @param array $arrValues The values array
	 *
	 * @return array The array with the escaped values
	 *
	 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
	 */
	protected function escapeParams($arrValues)
	{
		trigger_deprecation('contao/core-bundle', '4.13', 'Using "%s()" has been deprecated and will no longer work in Contao 5.0.', __METHOD__);

		foreach ($arrValues as $k=>$v)
		{
			switch (\gettype($v))
			{
				case 'string':
					$arrValues[$k] = $this->resConnection->quote($v);
					break;

				case 'boolean':
					$arrValues[$k] = ($v === true) ? 1 : 0;
					break;

				case 'object':
				case 'array':
					$arrValues[$k] = $this->resConnection->quote(serialize($v));
					break;

				default:
					$arrValues[$k] = $v ?? 'NULL';
					break;
			}
		}

		return $arrValues;
	}

	/**
	 * Explain the current query
	 *
	 * @return string The explanation string
	 *
	 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
	 */
	public function explain()
	{
		trigger_deprecation('contao/core-bundle', '4.13', 'Using "%s()" has been deprecated and will no longer work in Contao 5.0.', __METHOD__);

		return $this->resConnection->fetchAssociative('EXPLAIN ' . $this->strQuery, $this->arrLastUsedParams);
	}

	/**
	 * Bypass the cache and always execute the query
	 *
	 * @return Result The result object
	 *
	 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
	 *             Use Statement::execute() instead.
	 */
	public function executeUncached()
	{
		trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Statement::executeUncached()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Statement::execute()" instead.');

		return \call_user_func_array(array($this, 'execute'), \func_get_args());
	}

	/**
	 * Always execute the query and add or replace an existing cache entry
	 *
	 * @return Result The result object
	 *
	 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
	 *             Use Statement::execute() instead.
	 */
	public function executeCached()
	{
		trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\Statement::executeCached()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\Statement::execute()" instead.');

		return \call_user_func_array(array($this, 'execute'), \func_get_args());
	}
}
```

```php
namespace Contao\Database;

trigger_deprecation('contao/core-bundle', '4.0', 'Using the "Contao\Database\Updater" class has been deprecated and will no longer work in Contao 5.0.');

/**
 * Adjust the database if the system is updated.
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
 */
class Updater extends Controller
{
```

```php
namespace Contao;

class MemberGroupModel extends Model
{
/**
	 * Find the first active group with a published jumpTo page
	 *
	 * @param array $arrIds An array of member group IDs
	 *
	 * @return MemberGroupModel|null The model or null if there is no matching member group
	 *
	 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0.
	 *             Use PageModel::findFirstActiveByMemberGroups() instead.
	 */
	public static function findFirstActiveWithJumpToByIds($arrIds)
	{
		trigger_deprecation('contao/core-bundle', '4.0', 'Using "Contao\MemberGroupModel::findFirstActiveWithJumpToByIds()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\PageModel::findFirstActiveByMemberGroups()" instead.');

		if (empty($arrIds) || !\is_array($arrIds))
		{
			return null;
		}

		$time = Date::floorToMinute();
		$objDatabase = Database::getInstance();
		$arrIds = array_map('\intval', $arrIds);

		$objResult = $objDatabase->prepare("SELECT p.* FROM tl_member_group g LEFT JOIN tl_page p ON g.jumpTo=p.id WHERE g.id IN(" . implode(',', $arrIds) . ") AND g.jumpTo>0 AND g.redirect='1' AND g.disable!='1' AND (g.start='' OR g.start<=$time) AND (g.stop='' OR g.stop>$time) AND p.published='1' AND (p.start='' OR p.start<=$time) AND (p.stop='' OR p.stop>$time) ORDER BY " . $objDatabase->findInSet('g.id', $arrIds))
								 ->limit(1)
								 ->execute();

		if ($objResult->numRows < 1)
		{
			return null;
		}

		return new static($objResult);
```

```php
namespace Contao;

class OptInModel extends Model
{
/**
	 * Find an opt-in token by its related table and ID
	 *
	 * @param string  $strTable
	 * @param integer $intId
	 * @param array   $arrOptions
	 *
	 * @return static|null
	 *
	 * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.0; use the
	 *             Contao\OptInModel::findByRelatedTableAndIds() method instead
	 */
	public static function findOneByRelatedTableAndId($strTable, $intId, array $arrOptions=array())
	{
		trigger_deprecation('contao/core-bundle', '4.7', 'Using "Contao\OptInModel::findOneByRelatedTableAndIds()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\OptInModel::findByRelatedTableAndIds()" instead.');

		$t = static::$strTable;
		$objDatabase = Database::getInstance();

		$objResult = $objDatabase->prepare("SELECT * FROM $t WHERE id IN (SELECT pid FROM tl_opt_in_related WHERE relTable=? AND relId=?)")
								 ->execute($strTable, $intId);

		if ($objResult->numRows < 1)
		{
			return null;
		}

		$objRegistry = Registry::getInstance();

		/** @var OptInModel|Model $objOptIn */
		if ($objOptIn = $objRegistry->fetch($t, $objResult->id))
		{
			return $objOptIn;
		}

		return new static($objResult);
	}
```

```php
namespace Contao;

class PageModel extends Model
{
	/**
	 * Find the first published root page by its host name and language
	 *
	 * @param string $strHost     The host name
	 * @param mixed  $varLanguage An ISO language code or an array of ISO language codes
	 * @param array  $arrOptions  An optional options array
	 *
	 * @return PageModel|null The model or null if there is no matching root page
	 *
	 * @deprecated Deprecated since Contao 4.7, to be removed in Contao 5.0.
	 */
	public static function findFirstPublishedRootByHostAndLanguage($strHost, $varLanguage, array $arrOptions=array())
	{
		trigger_deprecation('contao/core-bundle', '4.7', 'Using "Contao\PageModel::findFirstPublishedRootByHostAndLanguage()" has been deprecated and will no longer work Contao 5.0.');

		$t = static::$strTable;
		$objDatabase = Database::getInstance();

		if (\is_array($varLanguage))
		{
			$arrColumns = array("$t.type='root' AND ($t.dns=? OR $t.dns='')");

			if (!empty($varLanguage))
			{
				$arrColumns[] = "($t.language IN('" . implode("','", $varLanguage) . "') OR $t.fallback='1')";
			}
			else
			{
				$arrColumns[] = "$t.fallback='1'";
			}

			if (!isset($arrOptions['order']))
			{
				$arrOptions['order'] = "$t.dns DESC" . (!empty($varLanguage) ? ", " . $objDatabase->findInSet("$t.language", array_reverse($varLanguage)) . " DESC" : "") . ", $t.sorting";
			}

			if (!static::isPreviewMode($arrOptions))
			{
				$time = Date::floorToMinute();
				$arrColumns[] = "$t.published='1' AND ($t.start='' OR $t.start<=$time) AND ($t.stop='' OR $t.stop>$time)";
			}

			return static::findOneBy($arrColumns, $strHost, $arrOptions);
		}

		$arrColumns = array("$t.type='root' AND ($t.dns=? OR $t.dns='') AND ($t.language=? OR $t.fallback='1')");
		$arrValues = array($strHost, $varLanguage);

		if (!isset($arrOptions['order']))
		{
			$arrOptions['order'] = "$t.dns DESC, $t.fallback";
		}

		if (!static::isPreviewMode($arrOptions))
		{
			$time = Date::floorToMinute();
			$arrColumns[] = "$t.published='1' AND ($t.start='' OR $t.start<=$time) AND ($t.stop='' OR $t.stop>$time)";
		}

		return static::findOneBy($arrColumns, $arrValues, $arrOptions);
	}

	/**
	 * Find all published subpages by their parent ID and exclude pages only visible for guests
	 *
	 * @param integer $intPid        The parent page's ID
	 * @param boolean $blnShowHidden If true, hidden pages will be included
	 * @param boolean $blnIsSitemap  If true, the sitemap settings apply
	 *
	 * @return Collection|PageModel[]|PageModel|null A collection of models or null if there are no pages
	 *
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0;
	 *             use PageModel::findPublishedByPid() instead and filter the guests pages yourself
	 */
	public static function findPublishedSubpagesWithoutGuestsByPid($intPid, $blnShowHidden=false, $blnIsSitemap=false)
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using PageModel::findPublishedSubpagesWithoutGuestsByPid() has been deprecated and will no longer work Contao 5.0. Use PageModel::findPublishedByPid() instead and filter the guests pages yourself.');

		$time = Date::floorToMinute();
		$tokenChecker = System::getContainer()->get('contao.security.token_checker');
		$blnFeUserLoggedIn = $tokenChecker->hasFrontendUser();
		$blnBeUserLoggedIn = $tokenChecker->isPreviewMode();
		$unroutableTypes = System::getContainer()->get('contao.routing.page_registry')->getUnroutableTypes();

		$objSubpages = Database::getInstance()->prepare("SELECT p1.*, (SELECT COUNT(*) FROM tl_page p2 WHERE p2.pid=p1.id AND p2.type!='root' AND p2.type NOT IN ('" . implode("', '", $unroutableTypes) . "')" . (!$blnShowHidden ? ($blnIsSitemap ? " AND (p2.hide='' OR sitemap='map_always')" : " AND p2.hide=''") : "") . ($blnFeUserLoggedIn ? " AND p2.guests=''" : "") . (!$blnBeUserLoggedIn ? " AND p2.published='1' AND (p2.start='' OR p2.start<=$time) AND (p2.stop='' OR p2.stop>$time)" : "") . ") AS subpages FROM tl_page p1 WHERE p1.pid=? AND p1.type!='root' AND p1.type NOT IN ('" . implode("', '", $unroutableTypes) . "')" . (!$blnShowHidden ? ($blnIsSitemap ? " AND (p1.hide='' OR sitemap='map_always')" : " AND p1.hide=''") : "") . ($blnFeUserLoggedIn ? " AND p1.guests=''" : "") . (!$blnBeUserLoggedIn ? " AND p1.published='1' AND (p1.start='' OR p1.start<=$time) AND (p1.stop='' OR p1.stop>$time)" : "") . " ORDER BY p1.sorting")
											  ->execute($intPid);

		if ($objSubpages->numRows < 1)
		{
			return null;
		}

		return static::createCollectionFromDbResult($objSubpages, 'tl_page');
	}

	/**
	 * Find all published regular pages by their IDs and exclude pages only visible for guests
	 *
	 * @param array $arrIds     An array of page IDs
	 * @param array $arrOptions An optional options array
	 *
	 * @return Collection|PageModel[]|PageModel|null A collection of models or null if there are no pages
	 *
	 * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5;
	 *             use PageModel::findPublishedRegularByIds() instead.
	 */
	public static function findPublishedRegularWithoutGuestsByIds($arrIds, array $arrOptions=array())
	{
		trigger_deprecation('contao/core-bundle', '4.12', 'Using PageModel::findPublishedRegularWithoutGuestsByIds() has been deprecated and will no longer work in Contao 5.0. Use PageModel::findPublishedRegularByIds() instead.');

		if (empty($arrIds) || !\is_array($arrIds))
		{
			return null;
		}

		$t = static::$strTable;
		$unroutableTypes = System::getContainer()->get('contao.routing.page_registry')->getUnroutableTypes();
		$arrColumns = array("$t.id IN(" . implode(',', array_map('\intval', $arrIds)) . ") AND $t.type NOT IN ('" . implode("', '", $unroutableTypes) . "')");

		if (empty($arrOptions['includeRoot']))
		{
			$arrColumns[] = "$t.type!='root'";
		}

		if (System::getContainer()->get('contao.security.token_checker')->hasFrontendUser())
		{
			$arrColumns[] = "$t.guests=''";
		}

		if (!static::isPreviewMode($arrOptions))
		{
			$time = Date::floorToMinute();
			$arrColumns[] = "$t.published='1' AND ($t.start='' OR $t.start<=$time) AND ($t.stop='' OR $t.stop>$time)";
		}

		if (!isset($arrOptions['order']))
		{
			$arrOptions['order'] = Database::getInstance()->findInSet("$t.id", $arrIds);
		}

		return static::findBy($arrColumns, null, $arrOptions);
	}
	/**
	 * Find all published regular pages by their parent IDs and exclude pages only visible for guests
	 *
	 * @param integer $intPid     The parent page's ID
	 * @param array   $arrOptions An optional options array
	 *
	 * @return Collection|PageModel[]|PageModel|null A collection of models or null if there are no pages
	 *
	 * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5;
	 *             use PageModel::findPublishedRegularByPid() instead.
	 */
	public static function findPublishedRegularWithoutGuestsByPid($intPid, array $arrOptions=array())
	{
		trigger_deprecation('contao/core-bundle', '4.12', 'Using PageModel::findPublishedRegularWithoutGuestsByPid() has been deprecated and will no longer work in Contao 5.0. Use PageModel::findPublishedRegularByPid() instead.');

		$t = static::$strTable;
		$unroutableTypes = System::getContainer()->get('contao.routing.page_registry')->getUnroutableTypes();
		$arrColumns = array("$t.pid=? AND $t.type!='root' AND $t.type NOT IN ('" . implode("', '", $unroutableTypes) . "')");

		if (System::getContainer()->get('contao.security.token_checker')->hasFrontendUser())
		{
			$arrColumns[] = "$t.guests=''";
		}

		if (!static::isPreviewMode($arrOptions))
		{
			$time = Date::floorToMinute();
			$arrColumns[] = "$t.published='1' AND ($t.start='' OR $t.start<=$time) AND ($t.stop='' OR $t.stop>$time)";
		}

		if (!isset($arrOptions['order']))
		{
			$arrOptions['order'] = "$t.sorting";
		}

		return static::findBy($arrColumns, $intPid, $arrOptions);
	}
```

```php
namespace Contao;

abstract class Module extends Frontend
{
	/**
	 * Get all published pages by their parent ID and exclude pages only visible for guests
	 *
	 * @param integer $intPid        The parent page's ID
	 * @param boolean $blnShowHidden If true, hidden pages will be included
	 * @param boolean $blnIsSitemap  If true, the sitemap settings apply
	 *
	 * @return array<array{page:PageModel,hasSubpages:bool}>|null
	 *
	 * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0;
	 *             use Module::getPublishedSubpagesByPid() instead and filter the guests pages yourself.
	 */
	protected static function getPublishedSubpagesWithoutGuestsByPid($intPid, $blnShowHidden=false, $blnIsSitemap=false): ?array
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using Module::getPublishedSubpagesWithoutGuestsByPid() has been deprecated and will no longer work Contao 5.0. Use Module::getPublishedSubpagesByPid() instead and filter the guests pages yourself.');

		$time = Date::floorToMinute();
		$tokenChecker = System::getContainer()->get('contao.security.token_checker');
		$blnFeUserLoggedIn = $tokenChecker->hasFrontendUser();
		$blnBeUserLoggedIn = $tokenChecker->isPreviewMode();
		$unroutableTypes = System::getContainer()->get('contao.routing.page_registry')->getUnroutableTypes();

		$arrPages = Database::getInstance()->prepare("SELECT p1.id, EXISTS(SELECT * FROM tl_page p2 WHERE p2.pid=p1.id AND p2.type!='root' AND p2.type NOT IN ('" . implode("', '", $unroutableTypes) . "')" . (!$blnShowHidden ? ($blnIsSitemap ? " AND (p2.hide='' OR sitemap='map_always')" : " AND p2.hide=''") : "") . ($blnFeUserLoggedIn ? " AND p2.guests=''" : "") . (!$blnBeUserLoggedIn ? " AND p2.published='1' AND (p2.start='' OR p2.start<=$time) AND (p2.stop='' OR p2.stop>$time)" : "") . ") AS hasSubpages FROM tl_page p1 WHERE p1.pid=? AND p1.type!='root' AND p1.type NOT IN ('" . implode("', '", $unroutableTypes) . "')" . (!$blnShowHidden ? ($blnIsSitemap ? " AND (p1.hide='' OR sitemap='map_always')" : " AND p1.hide=''") : "") . ($blnFeUserLoggedIn ? " AND p1.guests=''" : "") . (!$blnBeUserLoggedIn ? " AND p1.published='1' AND (p1.start='' OR p1.start<=$time) AND (p1.stop='' OR p1.stop>$time)" : "") . " ORDER BY p1.sorting")
										   ->execute($intPid)
										   ->fetchAllAssoc();

		if (\count($arrPages) < 1)
		{
			return null;
		}

		// Load models into the registry with a single query
		PageModel::findMultipleByIds(array_map(static function ($row) { return $row['id']; }, $arrPages));

		return array_map(
			static function (array $row): array
			{
				return array(
					'page' => PageModel::findByPk($row['id']),
					'hasSubpages' => (bool) $row['hasSubpages'],
				);
			},
			$arrPages
		);
	}
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.2', 'Using the logout module has been deprecated and will no longer work in Contao 5.0. Use the logout page instead.');

/**
 * Front end module "logout".
 *
 * @deprecated Deprecated since Contao 4.2, to be removed in Contao 5.0.
 *             Use the logout page instead.
 */
class ModuleLogout extends Module
{
```

```php
namespace Contao;

class PageError401 extends Frontend
{
/**
	 * Generate an error 401 page
	 *
	 * @param PageModel|integer|null $objRootPage
	 *
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5; use
	 *             the PageError401::getResponse() method instead
	 */
	public function generate($objRootPage=null)
	{
		trigger_deprecation('contao/core-bundle', '4.19', 'Using PageError401::generate() has been deprecated in Contao 4.9 and will be removed in Contao 5.0. Use the PageError401::getResponse() method instead.');

		if (is_numeric($objRootPage))
		{
			trigger_deprecation('contao/core-bundle', '4.13', 'Passing a numeric ID to PageError401::generate() has been deprecated and will no longer work in Contao 5.0.');
		}

		/** @var PageModel $objPage */
		global $objPage;

		$obj401 = $this->prepare($objRootPage);
		$objPage = $obj401->loadDetails();

		// Reset inherited cache timeouts (see #231)
		if (!$objPage->includeCache)
		{
			$objPage->cache = 0;
			$objPage->clientCache = 0;
		}

		/** @var PageRegular $objHandler */
		$objHandler = new $GLOBALS['TL_PTY']['regular']();

		header('HTTP/1.1 401 Unauthorized');
		$objHandler->generate($objPage);
	}
```

```php
namespace Contao;

class PageError403 extends Frontend
{
	/**
	 * Generate an error 403 page
	 *
	 * @param PageModel|integer|null $objRootPage
	 *
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5; use
	 *             the PageError403::getResponse() method instead
	 */
	public function generate($objRootPage=null)
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using PageError403::generate() has been deprecated in Contao 4.9 and will be removed in Contao 5.0. Use the PageError403::getResponse() method instead.');

		if (is_numeric($objRootPage))
		{
			trigger_deprecation('contao/core-bundle', '4.13', 'Passing a numeric ID to PageError403::generate() has been deprecated and will no longer work in Contao 5.0.');
		}

		/** @var PageModel $objPage */
		global $objPage;

		$obj403 = $this->prepare($objRootPage);
		$objPage = $obj403->loadDetails();

		// Reset inherited cache timeouts (see #231)
		if (!$objPage->includeCache)
		{
			$objPage->cache = 0;
			$objPage->clientCache = 0;
		}

		/** @var PageRegular $objHandler */
		$objHandler = new $GLOBALS['TL_PTY']['regular']();

		header('HTTP/1.1 403 Forbidden');
		$objHandler->generate($objPage);
	}
```

```php
namespace Contao;

class PageError404 extends Frontend
{
	/**
	 * Generate an error 404 page
	 *
	 * @param PageModel|null $page
	 *
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5; use
	 *             the PageError404::getResponse() method instead
	 */
	public function generate($page=null)
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using PageError404::generate() has been deprecated in Contao 4.9 and will be removed in Contao 5.0. Use the PageError404::getResponse() method instead.');

		/** @var PageModel $objPage */
		global $objPage;

		$obj404 = $this->prepare($page);
		$objPage = $obj404->loadDetails();

		// Reset inherited cache timeouts (see #231)
		if (!$objPage->includeCache)
		{
			$objPage->cache = 0;
			$objPage->clientCache = 0;
		}

		/** @var PageRegular $objHandler */
		$objHandler = new $GLOBALS['TL_PTY']['regular']();

		header('HTTP/1.1 404 Not Found');
		$objHandler->generate($objPage);
	}
```

```php
namespace Contao;

class PageForward extends Frontend
{
	/**
	 * Redirect to an internal page
	 *
	 * @param PageModel $objPage
	 *
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5; use
	 *             the PageForward::getResponse() method instead
	 */
	public function generate($objPage)
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using PageForward::generate() has been deprecated in Contao 4.9 and will be removed in Contao 5.0. Use the PageForward::getResponse() method instead.');

		$this->redirect($this->getForwardUrl($objPage), $this->getRedirectStatusCode($objPage));
	}
```

```php
namespace Contao;

class PageRedirect extends Frontend
{
	/**
	 * Redirect to an external page
	 *
	 * @param PageModel $objPage
	 *
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5; use
	 *             the PageRedirect::getResponse() method instead
	 */
	public function generate($objPage)
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using PageRedirect::generate() has been deprecated in Contao 4.9 and will be removed in Contao 5.0. Use the PageRedirect::getResponse() method instead.');

		$this->prepare($objPage);

		$url = UrlUtil::makeAbsolute(System::getContainer()->get('contao.insert_tag.parser')->replaceInline($objPage->url), Environment::get('path') . '/');

		$this->redirect($url, $this->getRedirectStatusCode($objPage));
	}
```

```php
namespace Contao;

class PageRegular extends Frontend
{
	/**
	 * Generate a regular page
	 *
	 * @param PageModel $objPage
	 * @param boolean   $blnCheckRequest
	 *
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5; use
	 *             the PageRegular::getResponse() method instead
	 */
	public function generate($objPage, $blnCheckRequest=false)
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using PageRegular::generate() has been deprecated in Contao 4.9 and will be removed in Contao 5.0. Use the PageRegular::getResponse() method instead.');

		$this->prepare($objPage);

		$this->Template->output($blnCheckRequest);
	}
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.12', 'Using the "Contao\PageRoot" class been deprecated and will no longer work in Contao 5.0. Use Symfony routing instead.');

class PageRoot extends Frontend
{
	/**
	 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5; use
	 *             the PageRoot::getResponse() method instead
	 */
	public function generate($rootPageId, $blnReturn=false, $blnPreferAlias=false)
	{
		trigger_deprecation('contao/core-bundle', '4.9', 'Using PageRoot::generate() has been deprecated in Contao 4.9 and will be removed in Contao 5.0. Use the PageRoot::getResponse() method instead.');

		if (!$blnReturn)
		{
			$this->redirect($this->getRedirectUrl($rootPageId));
		}

		$objNextPage = $this->getNextPage($rootPageId);

		return ($blnPreferAlias && $objNextPage->alias) ? $objNextPage->alias : $objNextPage->id;
	}
```

```js
// core-bundle/src/Resources/contao/themes/flexible
// hover.js

/**
 * Colorize a table row when hovering over it
 *
 * @param {object} el    The DOM element
 * @param {int}    state The current state
 *
 * @deprecated The Theme.hoverRow() function has been deprecated in Contao 4 and will be removed in Contao 5.
 *             Assign the CSS class "hover-row" instead.
 */
hoverRow: function(el, state) {
  var items = $(el).getChildren();
  for (var i=0; i<items.length; i++) {
    if (items[i].nodeName.toLowerCase() == 'td') {
      items[i].setStyle('background-color', (state ? '#fffce1' : ''));
    }
  }
  window.console && console.warn('The Theme.hoverRow() function has been deprecated in Contao 4 and will be removed in Contao 5. Assign the CSS class "hover-row" instead.');
},

/**
 * Colorize a layer when hovering over it
 *
 * @param {object} el    The DOM element
 * @param {int}    state The current state
 *
 * @deprecated The Theme.hoverDiv() function has been deprecated in Contao 4 and will be removed in Contao 5.
 *             Assign the CSS class "hover-div" instead.
 */
hoverDiv: function(el, state) {
  if (!state) {
    el.removeAttribute('data-visited');
  }
  $(el).setStyle('background-color', (state ? '#fffce1' : ''));
  window.console && console.warn('The Theme.hoverDiv() function has been deprecated in Contao 4 and will be removed in Contao 5. Assign the CSS class "hover-div" instead.');
},
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.13', 'Using the "Contao\FileSelector" class has been deprecated and will no longer work in Contao 5.0. Use the picker instead.');

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use the picker instead.
 */
class FileSelector extends Widget
{
```

```php
namespace Contao;

class ListWizard extends Widget
{
	/**
	 * Return a form to choose a CSV file and import it
	 *
	 * @param DataContainer $dc
	 *
	 * @return string
	 *
	 * @throws \Exception
	 * @throws ResponseException
	 *
	 * @deprecated Deprecated since Contao 4.3 to be removed in 5.0.
	 *             Use the Contao\CoreBundle\Controller\BackendCsvImportController service instead.
	 */
	public function importList(DataContainer $dc)
	{
		$response = System::getContainer()->get(BackendCsvImportController::class)->importListWizardAction($dc);

		if ($response instanceof RedirectResponse)
		{
			throw new ResponseException($response);
		}

		return $response->getContent();
	}
```

```php
namespace Contao;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use the picker instead.
 */
class PageSelector extends Widget
{
```

```php
namespace Contao;

class Password extends Widget
{
/**
	 * Generate the label of the confirmation field and return it as string
	 *
	 * @return string
	 *
	 * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0
	 */
	public function generateConfirmationLabel()
	{
		trigger_deprecation('contao/core-bundle', '4.12', 'Using "Contao\Password::generateConfirmationLabel()" has been deprecated and will no longer work in Contao 5.0.');

		return sprintf(
			'<label for="ctrl_%s_confirm" class="confirm%s">%s%s%s</label>',
			$this->strId,
			($this->strClass ? ' ' . $this->strClass : ''),
			($this->mandatory ? '<span class="invisible">' . $GLOBALS['TL_LANG']['MSC']['mandatory'] . ' </span>' : ''),
			$GLOBALS['TL_LANG']['MSC']['confirm'][0],
			($this->mandatory ? '<span class="mandatory">*</span>' : '')
		);
	}

	/**
	 * Generate the widget and return it as string
	 *
	 * @return string
	 *
	 * @deprecated Deprecated since Contao 4.12, to be removed in Contao 5.0
	 */
	public function generateConfirmation()
	{
		trigger_deprecation('contao/core-bundle', '4.12', 'Using "Contao\Password::generateConfirmation()" has been deprecated and will no longer work in Contao 5.0.');

		return sprintf(
			'<input type="password" name="%s_confirm" id="ctrl_%s_confirm" class="tl_text tl_password confirm%s" value="" placeholder="%s" autocomplete="new-password"%s onfocus="Backend.getScrollOffset()">%s',
			$this->strName,
			$this->strId,
			($this->strClass ? ' ' . $this->strClass : ''),
			($this->varValue ? '*****' : ''),
			$this->getAttributes(),
			((isset($GLOBALS['TL_LANG']['MSC']['confirm'][1]) && Config::get('showHelp')) ? "\n  " . '<p class="tl_help tl_tip">' . $GLOBALS['TL_LANG']['MSC']['confirm'][1] . '</p>' : '')
		);
	}
```

```php
namespace Contao;

class TableWizard extends Widget
{
	/**
	 * Return a form to choose a CSV file and import it
	 *
	 * @param DataContainer $dc
	 *
	 * @return string
	 *
	 * @throws \Exception
	 * @throws ResponseException
	 *
	 * @deprecated Deprecated since Contao 4.3 to be removed in 5.0.
	 *             Use the Contao\CoreBundle\Controller\BackendCsvImportController service instead.
	 */
	public function importTable(DataContainer $dc)
	{
		$response = System::getContainer()->get(BackendCsvImportController::class)->importTableWizardAction($dc);

		if ($response instanceof RedirectResponse)
		{
			throw new ResponseException($response);
		}

		return $response->getContent();
	}
```

```php
namespace Contao;

trigger_deprecation('contao/core-bundle', '4.13', 'Using the "Contao\TextStore" widget has been deprecated and will no longer work in Contao 5.0. Use the password widget instead.');

/**
 *
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use the password widget instead.
 */
class TextStore extends Widget
{
```

```js
// core-bundle/src/Resources/public
// core.js

toggleVisibility: function(el, id, table) {
  window.console && console.warn('AjaxRequest.toggleVisibility() is deprecated. Please use the new toggle operation.');
}

toggleFeatured: function(el, id) {
  window.console && console.warn('AjaxRequest.toggleFeatured() is deprecated. Please use the new toggle operation.');
}

/**
 * Open a new window
 *
 * @deprecated Use Backend.openModalWindow() instead
 */
openWindow: function(el, width, height) {

}

/**
 * Toggle the opacity of the paste buttons
 *
 * @deprecated Not required anymore
 */
blink: function() {}

/**
 * Initialize the mootools color picker
 *
 * @returns {boolean}
 *
 * @deprecated Not required anymore
 */
addColorPicker: function() {
  return true;
}

```

```php
namespace Contao\CoreBundle\Response;

use Symfony\Component\HttpFoundation\Response;

/**
 * Custom response class to support legacy entry points.
 *
 * @deprecated Deprecated since Contao 4.0, to be removed in Contao 5.0
 */
class InitializeControllerResponse extends Response
{
```

```php
namespace Contao\CoreBundle\Routing;

class ScopeMatcher
{
    /**
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
     *             ScopeMatcher::isContaoMainRequest() instead
     */
    public function isContaoMasterRequest(KernelEvent $event): bool
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using ScopeMatcher::isContaoMasterRequest() has been deprecated and will no longer work in Contao 5.0. Use ScopeMatcher::isContaoMainRequest() instead.');

        return $this->isContaoMainRequest($event);
    }

    /**
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
     *             ScopeMatcher::isBackendMainRequest() instead
     */
    public function isBackendMasterRequest(KernelEvent $event): bool
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using ScopeMatcher::isBackendMasterRequest() has been deprecated and will no longer work in Contao 5.0. Use ScopeMatcher::isBackendMainRequest() instead.');

        return $this->isBackendMainRequest($event);
    }

    /**
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
     *             ScopeMatcher::isFrontendMainRequest() instead
     */
    public function isFrontendMasterRequest(KernelEvent $event): bool
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using ScopeMatcher::isFrontendMasterRequest() has been deprecated and will no longer work in Contao 5.0. Use ScopeMatcher::isFrontendMainRequest() instead.');

        return $this->isFrontendMainRequest($event);
    }
```

```php
namespace Contao\CoreBundle\Security;

final class ContaoCorePermissions
{
    /**
     * @deprecated use USER_CAN_EDIT_FORM instead
     */
    public const USER_CAN_ACCESS_FORM = 'contao_user.forms';
```

```php
namespace Contao\CoreBundle\Security\Authentication;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use the new authenticator system instead.
 */
class ContaoLoginAuthenticationListener extends AbstractAuthenticationListener
{
```

```php
namespace Contao\CoreBundle\Security\Authentication\Provider;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0.
 *             Use the new authenticator system instead.
 */
class AuthenticationProvider extends DaoAuthenticationProvider
{
```

```php
namespace Contao\CoreBundle\Security\Logout;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
 *             the Symfony\Component\Security\Http\Event\LogoutEvent event instead
 */
class LogoutHandler implements LogoutHandlerInterface
{
```

```php
namespace Contao\CoreBundle\Security\Logout;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
 *             the Symfony\Component\Security\Http\Event\LogoutEvent event instead
 */
class LogoutSuccessHandler extends DefaultLogoutSuccessHandler
{
```

```php
namespace Contao\CoreBundle\Security\User;

class ContaoUserProvider implements UserProviderInterface, PasswordUpgraderInterface
{
    /**
     * @param mixed $username
     *
     * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0;
     *             use ContaoUserProvider::loadUserByIdentifier() instead
     */
    public function loadUserByUsername($username): User
    {
        trigger_deprecation('contao/core-bundle', '4.13', 'Using "ContaoUserProvider::loadUserByUsername()" has been deprecated and will no longer work in Contao 5.0. Use "ContaoUserProvider::loadUserByIdentifier()" instead.');

        return $this->loadUserByIdentifier((string) $username);
    }
```

```php
namespace Contao\CoreBundle\String;

class SimpleTokenParser implements LoggerAwareInterface
{
    /**
     * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0;
     *             use the parse() method instead
     */
    public function parseTokens(string $subject, array $tokens): string
    {
        trigger_deprecation('contao/core-bundle', '4.10', 'Using the parseTokens() method has been deprecated and will no longer work in Contao 5.0. Use the parse() method instead.');

        return $this->parse($subject, $tokens);
    }
```

```php
namespace Contao\CoreBundle\Util;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
 *             the Composer\InstalledVersions class instead
 */
class PackageUtil
```

```php
namespace Contao\CoreBundle\Util;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
 *             the Contao\CoreBundle\String\SimpleTokenExpressionLanguage class instead
 */
class SimpleTokenExpressionLanguage extends \Contao\CoreBundle\String\SimpleTokenExpressionLanguage
{
```

```php
namespace Contao\CoreBundle\Util;

/**
 * @deprecated Deprecated since Contao 4.13, to be removed in Contao 5.0; use
 *             the Contao\CoreBundle\String\SimpleTokenParser class instead
 */
class SimpleTokenParser extends \Contao\CoreBundle\String\SimpleTokenParser
{
```

```php
namespace Contao\CoreBundle\Tests\Fixtures\Database;

/**
 * @deprecated
 */
class DoctrineArrayStatement extends ArrayStatement
{
```

```php
namespace Contao\CoreBundle\Tests\Functional\app;

class AppKernel extends Kernel
{
    /**
     * @deprecated since Symfony 4.2, use getProjectDir() instead
     */
    public function getRootDir(): string
    {
        return __DIR__;
    }
```
