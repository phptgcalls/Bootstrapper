# photo

**Description** : *Photo*

**Layer** : 211

```tl
photo#fb197a65 flags:# has_stickers:flags.0?true id:long access_hash:long file_reference:bytes date:int sizes:Vector<PhotoSize> video_sizes:flags.1?Vector<VideoSize> dc_id:int = Photo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **has_stickers** | [`flags.0?true`](type/true) | Whether the photo has mask stickers attached to it |
| <mark>id</mark> | [`long`](type/long) | ID |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash |
| <mark>file_reference</mark> | [`bytes`](type/bytes) | file reference |
| <mark>date</mark> | [`int`](type/int) | Date of upload |
| <mark>sizes</mark> | [`Vector<PhotoSize>`](type/PhotoSize) | Available sizes for download |
| **video_sizes** | [`flags.1?Vector<VideoSize>`](type/VideoSize) | For animated profiles, the MPEG4 videos |
| <mark>dc_id</mark> | [`int`](type/int) | DC ID to use for download |

---

## Type

[Photo](type/Photo)

---

## Example

```php
$photo = $client->photo(
	has_stickers : true,
	id : -3253624085433810126,
	access_hash : 6356241100097010795,
	file_reference : '?iWLiveProto9?qG',
	date : 7,
	sizes : array(
		$client->photoSizeEmpty(
			type : 'CJuZy1vVHKRQ6oAi',
		),
		$client->photoSize(
			type : 'quPwz9BNjXvnbRCL',
			w : 66,
			h : 60,
			size : 100,
		),
		$client->photoCachedSize(
			type : '2xp6B0vPanEbQhFf',
			w : 61,
			h : 21,
			bytes : 'l??NLiveProto?v?4?',
		),
		$client->photoStrippedSize(
			type : 'RiCAELqVIuDBNsU4',
			bytes : '+?_!LiveProtoG??Q?',
		),
		$client->photoSizeProgressive(
			type : 'UIs2hCHoS8GQzjyE',
			w : 78,
			h : 41,
			sizes : array(77),
		),
		$client->photoPathSize(
			type : 'xqosY7mirBZWwLXu',
			bytes : '??jPLiveProto
S?',
		),
	),
	video_sizes : array(
		$client->videoSize(
			type : 'M3DIjvnOBfGr1Jah',
			w : 7,
			h : 79,
			size : 25,
			video_start_ts : 586597.943359375,
		),
		$client->videoSizeEmojiMarkup(
			emoji_id : 4223715945938030099,
			background_colors : array(47),
		),
		$client->videoSizeStickerMarkup(
			stickerset : $client->inputStickerSetEmpty(),
			sticker_id : -3868562982488392303,
			background_colors : array(24),
		),
	),
	dc_id : 94,
);
```