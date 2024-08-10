# contao/installation-bundle deprecations (4.13)

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
    contao.install_tool:
        alias: contao_installation.install_tool
        public: true
        deprecated:
            package: contao/installation-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao_installation.install_tool" instead.

    contao.install_tool_user:
        alias: contao_installation.install_tool_user
        public: true
        deprecated:
            package: contao/installation-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao_installation.install_tool_user" instead.

    contao.installer:
        alias: contao_installation.database.installer
        public: true
        deprecated:
            package: contao/installation-bundle
            version: 4.13
            message: Using the "%alias_id%" service ID has been deprecated and will no longer work in Contao 5.0. Please use "contao_installation.database.installer" instead.
```

### php-docs / annotations

```php
namespace Contao\InstallationBundle\Database;

trigger_deprecation('contao/installation-bundle', '4.9', 'Using the "Contao\InstallationBundle\Database\AbstractVersionUpdate" class has been deprecated and will no longer work in Contao 5.0. Use the "Contao\CoreBundle\Migration\AbstractMigration" class instead.');

/**
 * @deprecated Deprecated since Contao 4.9, to be removed in Contao 5.0; use the
 *             Contao\CoreBundle\Migration\AbstractMigration class instead
 */
abstract class AbstractVersionUpdate implements ContainerAwareInterface
{
```
