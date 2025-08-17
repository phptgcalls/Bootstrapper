# webPageAttributeStickerSet

**Description** : *Contains info about a stickerset », for a webPage preview of a stickerset deep link » (the webPage will have a type of telegram_stickerset)*

**Layer** : 211

```tl
webPageAttributeStickerSet#50cc03d3 flags:# emojis:flags.0?true text_color:flags.1?true stickers:Vector<Document> = WebPageAttribute;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **emojis** | [`flags.0?true`](type/true) | Whether this i s a custom emoji stickerset |
| **text_color** | [`flags.1?true`](type/true) | Whether the color of this TGS custom emoji stickerset should be changed to the text color when used in messages, the accent color if used as emoji status, white on chat photos, or another appropriate color based on context |
| <mark>stickers</mark> | [`Vector<Document>`](type/Document) | A subset of the stickerset in the stickerset |

---

## Type

[WebPageAttribute](type/WebPageAttribute)

---

## Example

```php
$webPageAttribute = $client->webPageAttributeStickerSet(
	emojis : true,
	text_color : true,
	stickers : array(
		$client->documentEmpty(
			id : -3195425530238303932,
		),
		$client->document(
			id : -7297466969766260571,
			access_hash : 798682378510664984,
			file_reference : 'ț??RLiveProto????',
			date : 98,
			mime_type : 'sq8atLRovfIyXmME',
			size : -5458351131368362898,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'q9Q6JVgkcGvDiowd',
				),
				$client->photoSize(
					type : 'Skqd5xIWwpmsRl0e',
					w : 90,
					h : 72,
					size : 84,
				),
				$client->photoCachedSize(
					type : 'NrDHAYikZ4Ufg983',
					w : 91,
					h : 38,
					bytes : 'CEU?LiveProto?-?)?',
				),
				$client->photoStrippedSize(
					type : 'VPWDgavkAodTl4Cp',
					bytes : 'u?kLiveProto?{D?I',
				),
				$client->photoSizeProgressive(
					type : 'pIm9O3ybJEKFcrWM',
					w : 0,
					h : 60,
					sizes : array(67),
				),
				$client->photoPathSize(
					type : 'uMA1vqWZ58LwKbGX',
					bytes : 'd???LiveProtoO[+,?',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'tbT3UlhO8xMopNdi',
					w : 60,
					h : 93,
					size : 36,
					video_start_ts : 87701.0849609375,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : -6803665975585546180,
					background_colors : array(58),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 4314446461467130502,
					background_colors : array(84),
				),
			),
			dc_id : 36,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 95,
					h : 66,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'VvncNGYte7jOEp20',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -48845.119140625,
					w : 75,
					h : 58,
					preload_prefix_size : 77,
					video_start_ts : 1888998.451171875,
					video_codec : 'Xv9TF14B2gRHC6Sc',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 33,
					title : 'wdb7ql490aHLENZx',
					performer : 'uQlpZTKydacC5bM8',
					waveform : '?Z?}LiveProtoZU??',
				),
				$client->documentAttributeFilename(
					file_name : 'hJUKZucjkbdoNl2D',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'Q3BLavklrptGXgRI',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```