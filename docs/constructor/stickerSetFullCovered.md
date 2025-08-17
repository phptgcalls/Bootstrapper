# stickerSetFullCovered

**Description** : *Stickerset preview with all stickers of the stickerset included.
Currently used only for custom emoji stickersets, to avoid a further call to messages.getStickerSet*

**Layer** : 211

```tl
stickerSetFullCovered#40d13c0e set:StickerSet packs:Vector<StickerPack> keywords:Vector<StickerKeyword> documents:Vector<Document> = StickerSetCovered;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>set</mark> | [`StickerSet`](type/StickerSet) | Stickerset |
| <mark>packs</mark> | [`Vector<StickerPack>`](type/StickerPack) | Emoji information about every sticker in the stickerset |
| <mark>keywords</mark> | [`Vector<StickerKeyword>`](type/StickerKeyword) | Keywords for some or every sticker in the stickerset |
| <mark>documents</mark> | [`Vector<Document>`](type/Document) | Stickers |

---

## Type

[StickerSetCovered](type/StickerSetCovered)

---

## Example

```php
$stickerSetCovered = $client->stickerSetFullCovered(
	set : $client->stickerSet(
		archived : true,
		official : true,
		masks : true,
		emojis : true,
		text_color : true,
		channel_emoji_status : true,
		creator : true,
		installed_date : 43,
		id : 3183828858900936973,
		access_hash : -6333974514565365982,
		title : '9sKxwB3i5oCmyUrX',
		short_name : 'hsqD2ckxyEjVf7IM',
		thumbs : array(
			$client->photoSizeEmpty(
				type : 'obAYgjHlBwmfL2Ka',
			),
			$client->photoSize(
				type : 'Y1lyjhPM9qbmu6Zd',
				w : 8,
				h : 55,
				size : 12,
			),
			$client->photoCachedSize(
				type : 'slTUxiWe6C92mGR3',
				w : 94,
				h : 49,
				bytes : '<?#?-LiveProto???ސ',
			),
			$client->photoStrippedSize(
				type : 'WVL5icNk9vx6zumI',
				bytes : '	5HP?LiveProto??u%u',
			),
			$client->photoSizeProgressive(
				type : 'ORl6rWh3b20zgaSA',
				w : 63,
				h : 4,
				sizes : array(78),
			),
			$client->photoPathSize(
				type : '0WZYwOVXqN41iTUk',
				bytes : '?ֵM?LiveProtom????',
			),
		),
		thumb_dc_id : 21,
		thumb_version : 69,
		thumb_document_id : -5345102967103387433,
		count : 76,
		hash : 59,
	),
	packs : array(
		$client->stickerPack(
			emoticon : 'XWy2gaTcKUiVeCOb',
			documents : array(-6675167450521438883),
		),
	),
	keywords : array(
		$client->stickerKeyword(
			document_id : -5094715323734298316,
			keyword : array('nS0XJEOpbrlCHoig'),
		),
	),
	documents : array(
		$client->documentEmpty(
			id : 2152044185100802694,
		),
		$client->document(
			id : 7424211398323712829,
			access_hash : 2644642711882635242,
			file_reference : '??j?LiveProto:lڐ^',
			date : 96,
			mime_type : 'tAJM0PQGHhej8Sfx',
			size : 5615674837152092446,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'OEpgyw9Mq2GJukR8',
				),
				$client->photoSize(
					type : 'unXgAQzav8sJ7Nl6',
					w : 22,
					h : 1,
					size : 39,
				),
				$client->photoCachedSize(
					type : 'GIjbJ4Kzh7MWF590',
					w : 35,
					h : 22,
					bytes : 'ZCZ?LiveProto?=??',
				),
				$client->photoStrippedSize(
					type : 'sgSPeKxHbWkVpf9O',
					bytes : '&?O??LiveProto?p7XI',
				),
				$client->photoSizeProgressive(
					type : 'Xu3m5HBxnNMAbGqY',
					w : 91,
					h : 97,
					sizes : array(13),
				),
				$client->photoPathSize(
					type : 'lZAkdK8FWbVQcfew',
					bytes : 'G7??LiveProto?w??\\',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'oSFTqP53NghECpcZ',
					w : 2,
					h : 43,
					size : 23,
					video_start_ts : -2038948.287109375,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 7691372427088781203,
					background_colors : array(40),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -3782612465738138539,
					background_colors : array(92),
				),
			),
			dc_id : 35,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 16,
					h : 95,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'gMGNBPUjYA3wyLkF',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -1276352.498046875,
					w : 69,
					h : 70,
					preload_prefix_size : 100,
					video_start_ts : -849431.0908203125,
					video_codec : 'PmBObFtjnisz6hwJ',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 66,
					title : 'rRVkvPanhDCHiQz3',
					performer : 'ADc6P3RJNYVGLXnl',
					waveform : '}??hLiveProto?|?',
				),
				$client->documentAttributeFilename(
					file_name : 'jbtSCU1ATxEaJG5f',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : '5MDtWLEA8vCBdXg7',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```