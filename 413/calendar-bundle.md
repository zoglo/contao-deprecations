# contao/calendar-bundle deprecations (4.13)

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

class Calendar extends Frontend
{
     /**
	 * @deprecated Deprecated since Contao 4.9, to be made private in Contao 5.0
	 */
    protected function addEvent($objEvent, $intStart, $intEnd, $strUrl, $strBase='', $isRepeated=false)
	{
		if (static::class !== self::class)
		{
			trigger_deprecation('contao/calendar-bundle', '4.9', 'Calling "%s()" from an extended class has been deprecated, it will be made private in Contao 5.0.', __METHOD__);
		}
```

```php
namespace Contao;

abstract class Events extends Module
{
    protected function addEvent($objEvents, $intStart, $intEnd, $intBegin, $intLimit, $intCalendar)
	{
		/** @var PageModel $objPage */
		global $objPage;

		// Backwards compatibility (4th argument was $strUrl)
		if (\func_num_args() > 6)
		{
			trigger_deprecation('contao/calendar-bundle', '4.0', 'Calling "Contao\Events::addEvent()" with 7 arguments has been deprecated and will no longer work in Contao 5.0. Do not pass $strUrl as 4th argument anymore.');

			$intLimit = func_get_arg(5);
			$intCalendar = func_get_arg(6);
		}
```

```php
namespace Contao;

class ModuleEventReader extends Events
{
    protected function compile()
	{
	    //...
		if ($this->overviewPage)
		{
			$this->Template->referer = PageModel::findById($this->overviewPage)->getFrontendUrl();
			$this->Template->back = $this->customLabel ?: $GLOBALS['TL_LANG']['MSC']['eventOverview'];
		}
		else
		{
			trigger_deprecation('contao/calendar-bundle', '4.13', 'If you do not select an overview page in the event reader module, the "go back" link will no longer be shown in Contao 5.0.');

			$this->Template->referer = 'javascript:history.go(-1)';
			$this->Template->back = $GLOBALS['TL_LANG']['MSC']['goBack'];
		}
```
