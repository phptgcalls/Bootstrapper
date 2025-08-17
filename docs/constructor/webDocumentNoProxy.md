# webDocumentNoProxy

**Description** : *Remote document that can be downloaded without proxying through telegram*

**Layer** : 211

```tl
webDocumentNoProxy#f9c8bcc6 url:string size:int mime_type:string attributes:Vector<DocumentAttribute> = WebDocument;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>url</mark> | [`string`](type/string) | Document URL |
| <mark>size</mark> | [`int`](type/int) | File size |
| <mark>mime_type</mark> | [`string`](type/string) | MIME type |
| <mark>attributes</mark> | [`Vector<DocumentAttribute>`](type/DocumentAttribute) | Attributes for media types |

---

## Type

[WebDocument](type/WebDocument)

---

## Example

```php
$webDocument = $client->webDocumentNoProxy(
	url : 'https://docs.liveproto.dev',
	size : 53,
	mime_type : 'tkCj6KbrpBNE8Rsi',
	attributes : array(
		$client->documentAttributeImageSize(
			w : 1,
			h : 58,
		),
		$client->documentAttributeAnimated(),
		$client->documentAttributeSticker(
			mask : true,
			alt : 'FKIQdwUehjGpgXvB',
			stickerset : $client->inputStickerSetEmpty(),
			mask_coords : $client->maskCoords(
				n : 95,
				x : -641783.7861328125,
				y : 1265067.0263671875,
				zoom : 184728.8916015625,
			),
		),
		$client->documentAttributeVideo(
			round_message : true,
			supports_streaming : true,
			nosound : true,
			duration : 818509.1435546875,
			w : 47,
			h : 0,
			preload_prefix_size : 73,
			video_start_ts : -1870570.9033203125,
			video_codec : '8xkAu63F5fKGTevp',
		),
		$client->documentAttributeAudio(
			voice : true,
			duration : 66,
			title : 'WFc0zPav9b7pfIjJ',
			performer : 'ijC7SzDXTGeE05Z1',
			waveform : ')?	?VLiveProto?o?',
		),
		$client->documentAttributeFilename(
			file_name : 'q8V0ctGuWEXS1Awn',
		),
		$client->documentAttributeHasStickers(),
		$client->documentAttributeCustomEmoji(
			free : true,
			text_color : true,
			alt : 'ohunIb5UA4dmseV9',
			stickerset : $client->inputStickerSetEmpty(),
		),
	),
);
```