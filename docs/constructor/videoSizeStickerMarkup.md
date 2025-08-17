# videoSizeStickerMarkup

**Description** : *An animated profile picture based on a sticker*

**Layer** : 211

```tl
videoSizeStickerMarkup#da082fe stickerset:InputStickerSet sticker_id:long background_colors:Vector<int> = VideoSize;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>stickerset</mark> | [`InputStickerSet`](type/InputStickerSet) | Stickerset |
| <mark>sticker_id</mark> | [`long`](type/long) | Sticker ID |
| <mark>background_colors</mark> | [`Vector<int>`](type/int) | 1, 2, 3 or 4 RBG-24 colors used to generate a solid (1), gradient (2) or freeform gradient (3, 4) background, similar to how fill wallpapers are generated. The rotation angle for gradient backgrounds is 0 |

---

## Type

[VideoSize](type/VideoSize)

---

## Example

```php
$videoSize = $client->videoSizeStickerMarkup(
	stickerset : $client->inputStickerSetEmpty(),
	sticker_id : -7388027362373204276,
	background_colors : array(60),
);
```