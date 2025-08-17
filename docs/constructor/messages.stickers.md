# messages.stickers

**Description** : *Found stickers*

**Layer** : 211

```tl
messages.stickers#30a6ec7e hash:long stickers:Vector<Document> = messages.Stickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>stickers</mark> | [`Vector<Document>`](type/Document) | Stickers |

---

## Type

[messages.Stickers](type/messages.Stickers)

---

## Example

```php
$messagesStickers = $client->messages->stickers(
	hash : 861690910009490077,
	stickers : array(
		$client->documentEmpty(
			id : 5321122434272779158,
		),
		$client->document(
			id : 1159238283273595966,
			access_hash : 7001095551568755363,
			file_reference : 'm???oLiveProto?d?Z',
			date : 10,
			mime_type : 'T7kCph1BqwVoWtdU',
			size : -6482216063022033837,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'zcCSf1X6ArPIJRx2',
				),
				$client->photoSize(
					type : 'KrhaXey3kpBMD7ls',
					w : 80,
					h : 92,
					size : 14,
				),
				$client->photoCachedSize(
					type : 'SYewBMh9TWJnvEFa',
					w : 47,
					h : 99,
					bytes : 'T?P?LiveProto???',
				),
				$client->photoStrippedSize(
					type : 'FdaOgME31kKQnThY',
					bytes : '?%#`?LiveProtoܕ?',
				),
				$client->photoSizeProgressive(
					type : 'UOryYjnZlhHiN9mF',
					w : 72,
					h : 8,
					sizes : array(81),
				),
				$client->photoPathSize(
					type : 'tEXxCOaWkh9l3DrZ',
					bytes : '4?u?~LiveProtor??@=',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'tErLZyISDWpx1hbG',
					w : 70,
					h : 68,
					size : 54,
					video_start_ts : -370849.3876953125,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : -6244943284152995076,
					background_colors : array(51),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -6291006180656425027,
					background_colors : array(99),
				),
			),
			dc_id : 3,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 47,
					h : 13,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'FKBJz2bVZw01jNPf',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -1313499.1337890625,
					w : 36,
					h : 95,
					preload_prefix_size : 51,
					video_start_ts : 1353451.158203125,
					video_codec : 'CmXPBuzVSEfdKL5G',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 48,
					title : 'xCk43wedUbSfBT6s',
					performer : 'jAL6ndaISTquxXFb',
					waveform : 'd1?-?LiveProto/6?m',
				),
				$client->documentAttributeFilename(
					file_name : 'QhsqtZdPIafnkXON',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'EpYPW9G5Rqe6a0yC',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```