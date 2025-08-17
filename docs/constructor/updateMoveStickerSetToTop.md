# updateMoveStickerSetToTop

**Description** : *A stickerset was just moved to top, see here for more info »*

**Layer** : 211

```tl
updateMoveStickerSetToTop#86fccf85 flags:# masks:flags.0?true emojis:flags.1?true stickerset:long = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **masks** | [`flags.0?true`](type/true) | This update is referring to a mask stickerset |
| **emojis** | [`flags.1?true`](type/true) | This update is referring to a custom emoji stickerset |
| <mark>stickerset</mark> | [`long`](type/long) | Stickerset ID |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateMoveStickerSetToTop(
	masks : true,
	emojis : true,
	stickerset : 1660095195420888032,
);
```