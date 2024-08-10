# contao/newsletter-bundle deprecations (4.13)

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

/**
 * @deprecated Deprecated since Contao 4.10, to be removed in Contao 5.0.
 *             Use class NewsletterDenyListModel instead.
 */
class NewsletterBlacklistModel extends NewsletterDenyListModel
{
	public function __construct($objResult = null)
	{
		trigger_deprecation('contao/newsletter-bundle', '4.10', 'Using the "Contao\NewsletterBlacklistModel" class has been deprecated and will no longer work in Contao 5.0. Use the "Contao\NewsletterDenyListModel" class instead.');

		parent::__construct($objResult);
	}
}
```

```php
namespace Contao;

class Newsletter extends Backend
{
	protected function sendNewsletter(Email $objEmail, Result $objNewsletter, $arrRecipient, $text, $html, $css=null)
	{
		// HOOK: add custom logic
		if (isset($GLOBALS['TL_HOOKS']['sendNewsletter']) && \is_array($GLOBALS['TL_HOOKS']['sendNewsletter']))
		{
			trigger_deprecation('contao/core-bundle', '4.13', 'Using the "sendNewsletter" hook has been deprecated and will no longer work in Contao 5.0. Use the SendNewsletterEvent instead.');

			foreach ($GLOBALS['TL_HOOKS']['sendNewsletter'] as $callback)
			{
				$this->import($callback[0]);
				$this->{$callback[0]}->{$callback[1]}($objEmail, $objNewsletter, $arrRecipient, $text, $html);
			}
		}
	}

```

```php
namespace Contao;

class ModuleNewsletterReader extends Module
{
    protected function compile()
	{
		$this->Template->content = '';

		if ($this->overviewPage)
		{
			$this->Template->referer = PageModel::findById($this->overviewPage)->getFrontendUrl();
			$this->Template->back = $this->customLabel ?: $GLOBALS['TL_LANG']['MSC']['nl_overview'];
		}
		else
		{
			trigger_deprecation('contao/newsletter-bundle', '4.13', 'If you do not select an overview page in the newsletter reader module, the "go back" link will no longer be shown in Contao 5.0.');

			$this->Template->referer = 'javascript:history.go(-1)';
			$this->Template->back = $GLOBALS['TL_LANG']['MSC']['goBack'];
		}
```
