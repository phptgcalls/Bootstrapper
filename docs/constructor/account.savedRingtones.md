# account.savedRingtones

**Description** : *A list of saved notification sounds*

**Layer** : 211

```tl
account.savedRingtones#c1e92cc5 hash:long ringtones:Vector<Document> = account.SavedRingtones;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>ringtones</mark> | [`Vector<Document>`](type/Document) | Saved notification sounds |

---

## Type

[account.SavedRingtones](type/account.SavedRingtones)

---

## Example

```php
$accountSavedRingtones = $client->account->savedRingtones(
	hash : -1650612577471609467,
	ringtones : array(
		$client->documentEmpty(
			id : 3104476013938303307,
		),
		$client->document(
			id : 6653804875330365137,
			access_hash : -8702713205346584295,
			file_reference : 't??2LiveProto^??A
',
			date : 10,
			mime_type : 'M9b0crY4N6ipBLIV',
			size : 8892255958367560015,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'IDUE8rL2AQzKwtpn',
				),
				$client->photoSize(
					type : '8kPdiYAv1mcHOWaz',
					w : 34,
					h : 29,
					size : 95,
				),
				$client->photoCachedSize(
					type : 'NvwcIfJZuOnE2L13',
					w : 54,
					h : 73,
					bytes : '?}?R?LiveProtoq?8q',
				),
				$client->photoStrippedSize(
					type : 'dFvcKgWx4PC1BpXQ',
					bytes : '??[LiveProtoyz??o',
				),
				$client->photoSizeProgressive(
					type : 'cfIKoxEnPWJwR1GT',
					w : 14,
					h : 57,
					sizes : array(24),
				),
				$client->photoPathSize(
					type : 'h1VLRH6twXrygOcm',
					bytes : 'A???LiveProtov??? ',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'FPnyAUdGM5Q4CJeN',
					w : 43,
					h : 10,
					size : 71,
					video_start_ts : 1172060.1728515625,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 1218327769644942848,
					background_colors : array(88),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 2077206100172673118,
					background_colors : array(17),
				),
			),
			dc_id : 23,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 56,
					h : 58,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'vEsD4qxGT1caAMLW',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -787334.2177734375,
					w : 43,
					h : 83,
					preload_prefix_size : 10,
					video_start_ts : 1607504.865234375,
					video_codec : '05ncryKbQSN4ZgVl',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 31,
					title : 'pbVt5Jme7MlNPvcQ',
					performer : '9e71xw6OkvgVPsIJ',
					waveform : 'K*??LiveProto4??W',
				),
				$client->documentAttributeFilename(
					file_name : 'oTdc27PQUpgeJ16a',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'MAQobmCg7DqK9zN4',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```