# messages.readFeaturedStickers

**Description** : *Mark new featured stickers as read*

**Layer** : 211

```tl
messages.readFeaturedStickers#5b118126 id:Vector<long> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`Vector<long>`](type/long) | IDs of stickersets to mark as read |

---

## Result

[Bool](type/Bool)

---

## Example

```php
$bool = $client->messages->readFeaturedStickers(
	id : array(2004738519883405330),
);
```