# stickers.replaceSticker

**Description** : *Replace a sticker in a stickerset »*

**Layer** : 211

```tl
stickers.replaceSticker#4696459a sticker:InputDocument new_sticker:InputStickerSetItem = messages.StickerSet;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>sticker</mark> | [`InputDocument`](type/InputDocument) | Old sticker document |
| <mark>new_sticker</mark> | [`InputStickerSetItem`](type/InputStickerSetItem) | New sticker |

---

## Result

[messages.StickerSet](type/messages.StickerSet)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **STICKER_INVALID** | `400` | The provided sticker is invalid |

---

## Example

```php
$messagesStickerSet = $client->stickers->replaceSticker(
	sticker : $client->inputDocumentEmpty(),
	new_sticker : $client->inputStickerSetItem(
		document : $client->inputDocumentEmpty(),
		emoji : '9dX3Sp0eWxhfLqMb',
		mask_coords : $client->maskCoords(
			n : 2,
			x : 185120.0400390625,
			y : 117105.0126953125,
			zoom : 1480916.0703125,
		),
		keywords : 'cEZ4O2iKu06LxUlM',
	),
);
```