# document

**Description** : *Document*

**Layer** : 211

```tl
document#8fd4c4d8 flags:# id:long access_hash:long file_reference:bytes date:int mime_type:string size:long thumbs:flags.0?Vector<PhotoSize> video_thumbs:flags.1?Vector<VideoSize> dc_id:int attributes:Vector<DocumentAttribute> = Document;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>id</mark> | [`long`](type/long) | Document ID |
| <mark>access_hash</mark> | [`long`](type/long) | Check sum, dependent on document ID |
| <mark>file_reference</mark> | [`bytes`](type/bytes) | File reference |
| <mark>date</mark> | [`int`](type/int) | Creation date |
| <mark>mime_type</mark> | [`string`](type/string) | MIME type |
| <mark>size</mark> | [`long`](type/long) | Size |
| **thumbs** | [`flags.0?Vector<PhotoSize>`](type/PhotoSize) | Thumbnails |
| **video_thumbs** | [`flags.1?Vector<VideoSize>`](type/VideoSize) | Video thumbnails |
| <mark>dc_id</mark> | [`int`](type/int) | DC ID |
| <mark>attributes</mark> | [`Vector<DocumentAttribute>`](type/DocumentAttribute) | Attributes |

---

## Type

[Document](type/Document)

---

## Example

```php
$document = $client->document(
	id : 7108515288073160592,
	access_hash : 6393359424021218621,
	file_reference : '??LiveProto|!?O',
	date : 0,
	mime_type : 'zb7jPQ1RaWOmqyHU',
	size : 5205593312548211292,
	thumbs : array(
		$client->photoSizeEmpty(
			type : 'Hub6a4Lysifp3ljI',
		),
		$client->photoSize(
			type : 'PZph4iJSs5dDOkHA',
			w : 79,
			h : 73,
			size : 81,
		),
		$client->photoCachedSize(
			type : '1zMnN9JtqoOjexRb',
			w : 11,
			h : 38,
			bytes : '??	?LiveProto,j???',
		),
		$client->photoStrippedSize(
			type : 'G7mVlwr5n06tH2gE',
			bytes : ')??ȡLiveProtor??Q',
		),
		$client->photoSizeProgressive(
			type : 'H8az9DKwb3VFcmv1',
			w : 61,
			h : 67,
			sizes : array(99),
		),
		$client->photoPathSize(
			type : 'VvH6BYyoCu3qD1fb',
			bytes : 'U?V/LiveProto??/v',
		),
	),
	video_thumbs : array(
		$client->videoSize(
			type : 'KBL2pA8aOdHCRyFr',
			w : 45,
			h : 43,
			size : 41,
			video_start_ts : 1267498.2978515625,
		),
		$client->videoSizeEmojiMarkup(
			emoji_id : -3489595114153848094,
			background_colors : array(72),
		),
		$client->videoSizeStickerMarkup(
			stickerset : $client->inputStickerSetEmpty(),
			sticker_id : -1849605934514637125,
			background_colors : array(58),
		),
	),
	dc_id : 92,
	attributes : array(
		$client->documentAttributeImageSize(
			w : 26,
			h : 43,
		),
		$client->documentAttributeAnimated(),
		$client->documentAttributeSticker(
			mask : true,
			alt : '3et07yspLKFZDJ9n',
			stickerset : $client->inputStickerSetEmpty(),
			mask_coords : $client->maskCoords(
				n : 37,
				x : -1592838.81640625,
				y : 1154192.9931640625,
				zoom : -1797123.03125,
			),
		),
		$client->documentAttributeVideo(
			round_message : true,
			supports_streaming : true,
			nosound : true,
			duration : -1903713.6064453125,
			w : 98,
			h : 54,
			preload_prefix_size : 76,
			video_start_ts : -919093.1875,
			video_codec : 'MKzOINLucUbP0ydW',
		),
		$client->documentAttributeAudio(
			voice : true,
			duration : 7,
			title : 'UAoK41aj6HurzLN3',
			performer : '0ERyFxDVaTQNJ4gK',
			waveform : 'a?J?LiveProto??j.',
		),
		$client->documentAttributeFilename(
			file_name : 'nXY2k3BfvwxMz6lZ',
		),
		$client->documentAttributeHasStickers(),
		$client->documentAttributeCustomEmoji(
			free : true,
			text_color : true,
			alt : 'GzFXc3CYwexH9kPZ',
			stickerset : $client->inputStickerSetEmpty(),
		),
	),
);
```