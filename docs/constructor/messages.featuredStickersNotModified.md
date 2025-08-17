# messages.featuredStickersNotModified

**Description** : *Featured stickers haven't changed*

**Layer** : 211

```tl
messages.featuredStickersNotModified#c6dc0c66 count:int = messages.FeaturedStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Total number of featured stickers |

---

## Type

[messages.FeaturedStickers](type/messages.FeaturedStickers)

---

## Example

```php
$messagesFeaturedStickers = $client->messages->featuredStickersNotModified(
	count : 40,
);
```