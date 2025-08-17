# videoSizeEmojiMarkup

**Description** : *An animated profile picture based on a custom emoji sticker*

**Layer** : 211

```tl
videoSizeEmojiMarkup#f85c413c emoji_id:long background_colors:Vector<int> = VideoSize;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>emoji_id</mark> | [`long`](type/long) | Custom emoji ID: the custom emoji sticker is shown at the center of the profile picture and occupies at most 67% of it |
| <mark>background_colors</mark> | [`Vector<int>`](type/int) | 1, 2, 3 or 4 RBG-24 colors used to generate a solid (1), gradient (2) or freeform gradient (3, 4) background, similar to how fill wallpapers are generated. The rotation angle for gradient backgrounds is 0 |

---

## Type

[VideoSize](type/VideoSize)

---

## Example

```php
$videoSize = $client->videoSizeEmojiMarkup(
	emoji_id : 7694604621845562011,
	background_colors : array(80),
);
```