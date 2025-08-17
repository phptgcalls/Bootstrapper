# messages.foundStickers

**Description** : *Found stickers*

**Layer** : 211

```tl
messages.foundStickers#82c9e290 flags:# next_offset:flags.0?int hash:long stickers:Vector<Document> = messages.FoundStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **next_offset** | [`flags.0?int`](type/int) | Offset for pagination |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>stickers</mark> | [`Vector<Document>`](type/Document) | Found stickers |

---

## Type

[messages.FoundStickers](type/messages.FoundStickers)

---

## Example

```php
$messagesFoundStickers = $client->messages->foundStickers(
	next_offset : 54,
	hash : 5096462518047552251,
	stickers : array(
		$client->documentEmpty(
			id : -904236302943203983,
		),
		$client->document(
			id : -2780496301753226550,
			access_hash : -562291615480938413,
			file_reference : 'h9??LiveProto>7 ?',
			date : 66,
			mime_type : '4WZflHMDdL5Csqgn',
			size : 1305351077847559342,
			thumbs : array(
				$client->photoSizeEmpty(
					type : '2tK4oUOpcYHzJBhb',
				),
				$client->photoSize(
					type : '5Tq4iadv1VtBEx2Z',
					w : 9,
					h : 15,
					size : 30,
				),
				$client->photoCachedSize(
					type : 'wvOKoC87SH9XxLen',
					w : 34,
					h : 98,
					bytes : '???cLiveProto???]?',
				),
				$client->photoStrippedSize(
					type : 'vd79MC0a1JA65pPw',
					bytes : 'iҠ?2LiveProto???',
				),
				$client->photoSizeProgressive(
					type : 'lsBumQYNEtIDG6Ky',
					w : 50,
					h : 74,
					sizes : array(59),
				),
				$client->photoPathSize(
					type : 'fNk7tBIF0Gb52XgO',
					bytes : '??\'6yLiveProto:?',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'UVPdZD2R1LrKo360',
					w : 61,
					h : 15,
					size : 70,
					video_start_ts : 1547525.498046875,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : -7302769785053123378,
					background_colors : array(30),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -2585551631589874161,
					background_colors : array(99),
				),
			),
			dc_id : 18,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 51,
					h : 38,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'LqbnHXWesAZ2Fah0',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -1579463.0068359375,
					w : 27,
					h : 23,
					preload_prefix_size : 100,
					video_start_ts : 489148.3046875,
					video_codec : 'QmCgULthRraxycDO',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 41,
					title : '4Zw3eConyKIkRDjz',
					performer : 'z2DV8qZRFdLueOx5',
					waveform : '?K5j?LiveProto(???X',
				),
				$client->documentAttributeFilename(
					file_name : 'aV2dMiPtHsplw7zO',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'K1ZCmPVQ4JDG8zjo',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```