# messages.favedStickers

**Description** : *Favorited stickers*

**Layer** : 211

```tl
messages.favedStickers#2cb51097 hash:long packs:Vector<StickerPack> stickers:Vector<Document> = messages.FavedStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>packs</mark> | [`Vector<StickerPack>`](type/StickerPack) | Emojis associated to stickers |
| <mark>stickers</mark> | [`Vector<Document>`](type/Document) | Favorited stickers |

---

## Type

[messages.FavedStickers](type/messages.FavedStickers)

---

## Example

```php
$messagesFavedStickers = $client->messages->favedStickers(
	hash : -6724138208425597883,
	packs : array(
		$client->stickerPack(
			emoticon : 'nwGcUoi8B23bpxEt',
			documents : array(-1380740875704718634),
		),
	),
	stickers : array(
		$client->documentEmpty(
			id : -298824104226938324,
		),
		$client->document(
			id : 4117947854961092194,
			access_hash : -6139496638835010174,
			file_reference : 'Ҧ`??LiveProto?3]?',
			date : 43,
			mime_type : 'jP0HqOxEvlWauyLY',
			size : 6364893231011703343,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'RZMVxy8s6dqFp1i0',
				),
				$client->photoSize(
					type : 'Ms1LVCr367oJtAkW',
					w : 74,
					h : 51,
					size : 49,
				),
				$client->photoCachedSize(
					type : 'pRhwIs2nML6aWrlv',
					w : 75,
					h : 94,
					bytes : 'P?y\'LiveProtoa???',
				),
				$client->photoStrippedSize(
					type : '4qJWbnij2SGECAYX',
					bytes : 'K???yLiveProto,?y?@',
				),
				$client->photoSizeProgressive(
					type : 'StGPku4n6zNBR5C8',
					w : 32,
					h : 51,
					sizes : array(91),
				),
				$client->photoPathSize(
					type : 'HlbCTAy0Uxhn62Ff',
					bytes : '?z,?LiveProto?%o?',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'espjhF96xd83Cf2S',
					w : 31,
					h : 71,
					size : 17,
					video_start_ts : -629644.0166015625,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 8302505969164843493,
					background_colors : array(88),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 1879978527391451250,
					background_colors : array(3),
				),
			),
			dc_id : 77,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 47,
					h : 2,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'HPfUFV2uS0rOGo8E',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 438980.3447265625,
					w : 4,
					h : 46,
					preload_prefix_size : 64,
					video_start_ts : -800319.583984375,
					video_codec : 'F2xk0Ur8QBgYlXOf',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 12,
					title : 'ciJaqv8KrI69Rk0b',
					performer : 'FpDiSlj7601ukhIW',
					waveform : 'ԉ?`LiveProto)??a?',
				),
				$client->documentAttributeFilename(
					file_name : 'tFyUxlEr13TZuN64',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'qPi4rBF0OCzWYQvS',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```