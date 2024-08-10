# contao/faq-bundle deprecations (4.13)

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

class ModuleFaqReader extends Module
{
	protected function compile()
	{
		/** @var PageModel $objPage */
		global $objPage;

		if ($this->overviewPage)
		{
			$this->Template->referer = PageModel::findById($this->overviewPage)->getFrontendUrl();
			$this->Template->back = $this->customLabel ?: $GLOBALS['TL_LANG']['MSC']['faqOverview'];
		}
		else
		{
			trigger_deprecation('contao/faq-bundle', '4.13', 'If you do not select an overview page in the FAQ reader module, the "go back" link will no longer be shown in Contao 5.0.');

			$this->Template->back = $GLOBALS['TL_LANG']['MSC']['goBack'];
			$this->Template->referer = 'javascript:history.go(-1)';
		}
```
