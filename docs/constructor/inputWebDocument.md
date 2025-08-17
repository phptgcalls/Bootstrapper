# inputWebDocument

**Description** : *The document*

**Layer** : 211

```tl
inputWebDocument#9bed434d url:string size:int mime_type:string attributes:Vector<DocumentAttribute> = InputWebDocument;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>url</mark> | [`string`](type/string) | Remote document URL to be downloaded using the appropriate method |
| <mark>size</mark> | [`int`](type/int) | Remote file size |
| <mark>mime_type</mark> | [`string`](type/string) | Mime type |
| <mark>attributes</mark> | [`Vector<DocumentAttribute>`](type/DocumentAttribute) | Attributes for media types |

---

## Type

[InputWebDocument](type/InputWebDocument)

---

## Example

```php
$inputWebDocument = $client->inputWebDocument(
	url : 'https://docs.liveproto.dev',
	size : 98,
	mime_type : 'hnsMcbl5mTKvZ3LA',
	attributes : array(
		$client->documentAttributeImageSize(
			w : 39,
			h : 91,
		),
		$client->documentAttributeAnimated(),
		$client->documentAttributeSticker(
			mask : true,
			alt : 'IpY0uotePEmDQNSA',
			stickerset : $client->inputStickerSetEmpty(),
			mask_coords : $client->maskCoords(
				n : 15,
				x : 1873247.962890625,
				y : 445754.1201171875,
				zoom : 273456.1142578125,
			),
		),
		$client->documentAttributeVideo(
			round_message : true,
			supports_streaming : true,
			nosound : true,
			duration : 1579178.365234375,
			w : 25,
			h : 72,
			preload_prefix_size : 0,
			video_start_ts : 822149.001953125,
			video_codec : '6tQTvklmI7NnoWMJ',
		),
		$client->documentAttributeAudio(
			voice : true,
			duration : 91,
			title : 'hxQedSJR0uYpi2P9',
			performer : 'C3b8ROgcsdo9YB5j',
			waveform : 'rܴ\\]LiveProto*???m',
		),
		$client->documentAttributeFilename(
			file_name : 'TRZYerOxBq9MHIbW',
		),
		$client->documentAttributeHasStickers(),
		$client->documentAttributeCustomEmoji(
			free : true,
			text_color : true,
			alt : 'jTV7Yz9DaZymxufp',
			stickerset : $client->inputStickerSetEmpty(),
		),
	),
);
```