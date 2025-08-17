# webDocument

**Description** : *Remote document*

**Layer** : 211

```tl
webDocument#1c570ed1 url:string access_hash:long size:int mime_type:string attributes:Vector<DocumentAttribute> = WebDocument;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>url</mark> | [`string`](type/string) | Document URL |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash |
| <mark>size</mark> | [`int`](type/int) | File size |
| <mark>mime_type</mark> | [`string`](type/string) | MIME type |
| <mark>attributes</mark> | [`Vector<DocumentAttribute>`](type/DocumentAttribute) | Attributes for media types |

---

## Type

[WebDocument](type/WebDocument)

---

## Example

```php
$webDocument = $client->webDocument(
	url : 'https://docs.liveproto.dev',
	access_hash : -3992288160249455908,
	size : 20,
	mime_type : 'lgzajSEH3XQ4t5pn',
	attributes : array(
		$client->documentAttributeImageSize(
			w : 8,
			h : 24,
		),
		$client->documentAttributeAnimated(),
		$client->documentAttributeSticker(
			mask : true,
			alt : 'CMjKYTlHbkgt3W8V',
			stickerset : $client->inputStickerSetEmpty(),
			mask_coords : $client->maskCoords(
				n : 13,
				x : -1105824.5654296875,
				y : -1757383.009765625,
				zoom : -564479.82421875,
			),
		),
		$client->documentAttributeVideo(
			round_message : true,
			supports_streaming : true,
			nosound : true,
			duration : -1801944.9580078125,
			w : 48,
			h : 30,
			preload_prefix_size : 52,
			video_start_ts : -1648801.705078125,
			video_codec : 'yGlAr5bZgURtPLqT',
		),
		$client->documentAttributeAudio(
			voice : true,
			duration : 24,
			title : 'SqEFtBQKjaP264Jm',
			performer : 'NvoMfyIjBPYXWDaK',
			waveform : 'Iel?"LiveProtof????',
		),
		$client->documentAttributeFilename(
			file_name : 'n3RrPCx7oMiykHhu',
		),
		$client->documentAttributeHasStickers(),
		$client->documentAttributeCustomEmoji(
			free : true,
			text_color : true,
			alt : 'hYGQJVrslze6EWBf',
			stickerset : $client->inputStickerSetEmpty(),
		),
	),
);
```