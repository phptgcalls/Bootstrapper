# messages.stickerSet

**Description** : *Stickerset and stickers inside it*

**Layer** : 211

```tl
messages.stickerSet#6e153f16 set:StickerSet packs:Vector<StickerPack> keywords:Vector<StickerKeyword> documents:Vector<Document> = messages.StickerSet;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>set</mark> | [`StickerSet`](type/StickerSet) | The stickerset |
| <mark>packs</mark> | [`Vector<StickerPack>`](type/StickerPack) | Emoji info for stickers |
| <mark>keywords</mark> | [`Vector<StickerKeyword>`](type/StickerKeyword) | Keywords for some or every sticker in the stickerset |
| <mark>documents</mark> | [`Vector<Document>`](type/Document) | Stickers in stickerset |

---

## Type

[messages.StickerSet](type/messages.StickerSet)

---

## Example

```php
$messagesStickerSet = $client->messages->stickerSet(
	set : $client->stickerSet(
		archived : true,
		official : true,
		masks : true,
		emojis : true,
		text_color : true,
		channel_emoji_status : true,
		creator : true,
		installed_date : 89,
		id : 4724659029814182924,
		access_hash : -9158972335602213289,
		title : 'hJUPLiIcAFuBpgfo',
		short_name : 'PDfVG3FAQ1X4amgZ',
		thumbs : array(
			$client->photoSizeEmpty(
				type : 'MDvX8c9bW6oj45N1',
			),
			$client->photoSize(
				type : '7mQZLY3PRfykw4TJ',
				w : 25,
				h : 47,
				size : 74,
			),
			$client->photoCachedSize(
				type : 'P38qtpuKnk47hO1D',
				w : 84,
				h : 94,
				bytes : 'B?]??LiveProtoN??A?',
			),
			$client->photoStrippedSize(
				type : 'SDb5FvwY9sU2GdLn',
				bytes : '???ߊLiveProto?1??~',
			),
			$client->photoSizeProgressive(
				type : '5gpuYoz3OTFhIt84',
				w : 38,
				h : 9,
				sizes : array(12),
			),
			$client->photoPathSize(
				type : 'f9NBCWtdLGXsDzqx',
				bytes : 'g?H:LiveProto????',
			),
		),
		thumb_dc_id : 58,
		thumb_version : 10,
		thumb_document_id : 1136387963900905704,
		count : 46,
		hash : 3,
	),
	packs : array(
		$client->stickerPack(
			emoticon : 'YDvyJ7kQ5udaof9r',
			documents : array(6823237142949866396),
		),
	),
	keywords : array(
		$client->stickerKeyword(
			document_id : 2919729575369575845,
			keyword : array('JRGq93IQbK2oVwCv'),
		),
	),
	documents : array(
		$client->documentEmpty(
			id : 4947905372958284649,
		),
		$client->document(
			id : 2439127836131855635,
			access_hash : -8489582309069334018,
			file_reference : 'L?ۘLiveProtoe?#?',
			date : 69,
			mime_type : 'SfaL6F29oUremK78',
			size : 6969723195107833981,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'Ng5l3nVCxJUKqE7w',
				),
				$client->photoSize(
					type : 'YH6VyEo2Fkwq8xbD',
					w : 35,
					h : 6,
					size : 67,
				),
				$client->photoCachedSize(
					type : 'Gj3WyzswtdHapEfY',
					w : 84,
					h : 71,
					bytes : '?t?LiveProto?g?f?',
				),
				$client->photoStrippedSize(
					type : '5C3lrdbZ29qYhFHL',
					bytes : '?^@?LiveProtoHˤ??',
				),
				$client->photoSizeProgressive(
					type : 'HNKQnURvO8FaufGr',
					w : 92,
					h : 0,
					sizes : array(98),
				),
				$client->photoPathSize(
					type : 'WSwNY63o5M8gR9PL',
					bytes : '@|?ωLiveProto锁?',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'nKURtbgcrOaNVCfB',
					w : 12,
					h : 50,
					size : 96,
					video_start_ts : -1496810.326171875,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 3994422157922549135,
					background_colors : array(40),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -3328642460794436548,
					background_colors : array(47),
				),
			),
			dc_id : 22,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 28,
					h : 12,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'fu0CvGIkbRpLNZXH',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 1215150.658203125,
					w : 90,
					h : 44,
					preload_prefix_size : 70,
					video_start_ts : -1839122.9736328125,
					video_codec : 'ywOh53BmIbU049KX',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 24,
					title : 'YUJPC718v4tAiTe2',
					performer : '2pR4y9JhScjWHvNe',
					waveform : 'l???LiveProto*?DPU',
				),
				$client->documentAttributeFilename(
					file_name : 'vAlUH1Se43FpPytr',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'Bl3tIz4XgU8hqpGV',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```