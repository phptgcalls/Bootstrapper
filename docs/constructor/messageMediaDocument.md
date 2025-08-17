# messageMediaDocument

**Description** : *Document (video, audio, voice, sticker, any media type except photo)*

**Layer** : 211

```tl
messageMediaDocument#52d8ccd9 flags:# nopremium:flags.3?true spoiler:flags.4?true video:flags.6?true round:flags.7?true voice:flags.8?true document:flags.0?Document alt_documents:flags.5?Vector<Document> video_cover:flags.9?Photo video_timestamp:flags.10?int ttl_seconds:flags.2?int = MessageMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **nopremium** | [`flags.3?true`](type/true) | Whether this is a normal sticker, if not set this is a premium sticker and a premium sticker animation must be played |
| **spoiler** | [`flags.4?true`](type/true) | Whether this media should be hidden behind a spoiler warning |
| **video** | [`flags.6?true`](type/true) | Whether this is a video |
| **round** | [`flags.7?true`](type/true) | Whether this is a round video |
| **voice** | [`flags.8?true`](type/true) | Whether this is a voice message |
| **document** | [`flags.0?Document`](type/Document) | Attached document |
| **alt_documents** | [`flags.5?Vector<Document>`](type/Document) | Videos only, contains alternative qualities of the video |
| **video_cover** | [`flags.9?Photo`](type/Photo) | NOTHING |
| **video_timestamp** | [`flags.10?int`](type/int) | NOTHING |
| **ttl_seconds** | [`flags.2?int`](type/int) | Time to live of self-destructing document |

---

## Type

[MessageMedia](type/MessageMedia)

---

## Example

```php
$messageMedia = $client->messageMediaDocument(
	nopremium : true,
	spoiler : true,
	video : true,
	round : true,
	voice : true,
	document : $client->documentEmpty(
		id : -2577108665611132510,
	),
	alt_documents : array(
		$client->documentEmpty(
			id : -8181835546174198130,
		),
		$client->document(
			id : -5431662325652893844,
			access_hash : 4868643150900089186,
			file_reference : '1%*?LiveProto?? ??',
			date : 64,
			mime_type : 'O4mj3N67SDuIYrXB',
			size : 7097564732358066227,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'o2CNYGIFgdbku86z',
				),
				$client->photoSize(
					type : 'fRihDTI7yXgvbS0d',
					w : 63,
					h : 51,
					size : 89,
				),
				$client->photoCachedSize(
					type : 'JvQOzhGLnjpsuHN2',
					w : 21,
					h : 78,
					bytes : '??6LiveProtog;̏?',
				),
				$client->photoStrippedSize(
					type : 'bOhigoW4LFsEV3Jp',
					bytes : '??cp?LiveProto??Č?',
				),
				$client->photoSizeProgressive(
					type : '5BJ8OkWuDXmr6LEy',
					w : 50,
					h : 86,
					sizes : array(72),
				),
				$client->photoPathSize(
					type : 'fBSuKPes4IvENXVl',
					bytes : 'ˏ?\\?LiveProto?3??',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'ptqu32sQL9dbvgO8',
					w : 100,
					h : 92,
					size : 85,
					video_start_ts : 537652.515625,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : -5582608685119421652,
					background_colors : array(0),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 2854137975237823479,
					background_colors : array(51),
				),
			),
			dc_id : 63,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 34,
					h : 81,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 't3Dv8gIZ41G0Xcwu',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 150703.125,
					w : 12,
					h : 80,
					preload_prefix_size : 45,
					video_start_ts : -1390360.1318359375,
					video_codec : 'KkpWxGdD6UjEm2tq',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 88,
					title : 'cH5UZhXVKmM23Gz0',
					performer : 'AB1eay8o7UjQEcbD',
					waveform : '??HLiveProto??\\?E',
				),
				$client->documentAttributeFilename(
					file_name : 'OMvKtb86G7h3VCau',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'S4G9EObscCgaJrli',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
	video_cover : $client->photoEmpty(
		id : -5118254147590116685,
	),
	video_timestamp : 43,
	ttl_seconds : 31,
);
```