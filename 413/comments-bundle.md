# contao/comments-bundle deprecations (4.13)

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

```php
namespace Contao;

class Comments extends Frontend
{
    protected function renderCommentForm(FrontendTemplate $objTemplate, \stdClass $objConfig, $strSource, $intParent, $varNotifies)
	{
        //...
        $objTemplate->messages = ''; // Deprecated since Contao 4.0, to be removed in Contao 5.0
```
