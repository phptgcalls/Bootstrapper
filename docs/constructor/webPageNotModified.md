# webPageNotModified

**Description** : *The preview of the webpage hasn't changed*

**Layer** : 211

```tl
webPageNotModified#7311ca11 flags:# cached_page_views:flags.0?int = WebPage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **cached_page_views** | [`flags.0?int`](type/int) | Page view count |

---

## Type

[WebPage](type/WebPage)

---

## Example

```php
$webPage = $client->webPageNotModified(
	cached_page_views : 22,
);
```