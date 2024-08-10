# contao/comments-bundle deprecations (4.13)

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

```php
namespace Contao;

class Comments extends Frontend
{
    protected function renderCommentForm(FrontendTemplate $objTemplate, \stdClass $objConfig, $strSource, $intParent, $varNotifies)
	{
        //...
        $objTemplate->messages = ''; // Deprecated since Contao 4.0, to be removed in Contao 5.0
```
