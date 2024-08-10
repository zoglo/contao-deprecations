# contao/news-bundle deprecations (4.13)

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

abstract class ModuleNews extends Module
{
	/**
	 * Generate a URL and return it as string
	 *
	 * @deprecated Deprecated since Contao 4.1, to be removed in Contao 5.
	 *             Use News::generateNewsUrl() instead.
	 */
	protected function generateNewsUrl($objItem, $blnAddArchive=false)
	{
		trigger_deprecation('contao/news-bundle', '4.1', 'Using "Contao\ModuleNews::generateNewsUrl()" has been deprecated and will no longer work in Contao 5.0. Use "Contao\News::generateNewsUrl()" instead.');

		return News::generateNewsUrl($objItem, $blnAddArchive);
	}
```

```php
namespace Contao;

class ModuleNewsReader extends ModuleNews
{
    protected function compile()
	{
		$this->Template->articles = '';

		if ($this->overviewPage)
		{
			$this->Template->referer = PageModel::findById($this->overviewPage)->getFrontendUrl();
			$this->Template->back = $this->customLabel ?: $GLOBALS['TL_LANG']['MSC']['newsOverview'];
		}
		else
		{
			trigger_deprecation('contao/news-bundle', '4.13', 'If you do not select an overview page in the news reader module, the "go back" link will no longer be shown in Contao 5.0.');

			$this->Template->referer = 'javascript:history.go(-1)';
			$this->Template->back = $GLOBALS['TL_LANG']['MSC']['goBack'];
		}
```
