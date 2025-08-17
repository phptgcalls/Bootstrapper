# stickerSetMultiCovered

**Description** : *Stickerset, with multiple stickers as preview*

**Layer** : 211

```tl
stickerSetMultiCovered#3407e51b set:StickerSet covers:Vector<Document> = StickerSetCovered;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>set</mark> | [`StickerSet`](type/StickerSet) | Stickerset |
| <mark>covers</mark> | [`Vector<Document>`](type/Document) | Preview stickers |

---

## Type

[StickerSetCovered](type/StickerSetCovered)

---

## Example

```php
$stickerSetCovered = $client->stickerSetMultiCovered(
	set : $client->stickerSet(
		archived : true,
		official : true,
		masks : true,
		emojis : true,
		text_color : true,
		channel_emoji_status : true,
		creator : true,
		installed_date : 12,
		id : 4794181054978616640,
		access_hash : 879494417280830656,
		title : '3dnzeiQtBNCWY0Tu',
		short_name : 'o45rekxVgLI0Us3G',
		thumbs : array(
			$client->photoSizeEmpty(
				type : '2bNjXACYFwUEemkD',
			),
			$client->photoSize(
				type : 'oSnswT4zbKqvVdAp',
				w : 2,
				h : 42,
				size : 76,
			),
			$client->photoCachedSize(
				type : 'VhyXBjQ1tG2Wnexs',
				w : 61,
				h : 98,
				bytes : '?c??5LiveProtoG#N?',
			),
			$client->photoStrippedSize(
				type : 'FrXocuEw6OpNDJjQ',
				bytes : '?k?tpLiveProto˺f??',
			),
			$client->photoSizeProgressive(
				type : 'aOR5xTGtsDQfVby9',
				w : 53,
				h : 28,
				sizes : array(71),
			),
			$client->photoPathSize(
				type : 'de0nm8tL9O15IAgv',
				bytes : ':??SbLiveProto??L??',
			),
		),
		thumb_dc_id : 62,
		thumb_version : 47,
		thumb_document_id : -6670721470854228107,
		count : 28,
		hash : 60,
	),
	covers : array(
		$client->documentEmpty(
			id : -6497289201864061589,
		),
		$client->document(
			id : 6823830665893597483,
			access_hash : -7859998542523159851,
			file_reference : 'P??8?LiveProto??]7',
			date : 24,
			mime_type : 'vJo8NuYmjlZ29MPU',
			size : -2201064087642303679,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'JpNAlm7Gaz1jCkxL',
				),
				$client->photoSize(
					type : 'DhcXSaoId9xwmpYi',
					w : 33,
					h : 64,
					size : 21,
				),
				$client->photoCachedSize(
					type : 'PZI14z3uNWDXgjfJ',
					w : 21,
					h : 37,
					bytes : '?e?L?LiveProto?D?~?',
				),
				$client->photoStrippedSize(
					type : 'bqVvDYIPNuClTa3M',
					bytes : 'u<??LiveProto?1',
				),
				$client->photoSizeProgressive(
					type : 'tQm2Wij4nrdvDcky',
					w : 74,
					h : 12,
					sizes : array(63),
				),
				$client->photoPathSize(
					type : 'SWdp1VctALk5DQyK',
					bytes : '!(VLiveProto;<?%:',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'ka5dUR8nSvOhs1b9',
					w : 25,
					h : 82,
					size : 75,
					video_start_ts : -1448341.49609375,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : -2756876911887324936,
					background_colors : array(62),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -1495126612691887271,
					background_colors : array(31),
				),
			),
			dc_id : 27,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 11,
					h : 75,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'omWghxBbZ1KUc3Oq',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 1384072.0546875,
					w : 15,
					h : 60,
					preload_prefix_size : 10,
					video_start_ts : -1145707.8994140625,
					video_codec : 'pbWB3Kxm2wLigq7G',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 96,
					title : 'o4IUt8zLPJgZOBxq',
					performer : 'ENvsGQKJH02h4Cmq',
					waveform : '?]Q?LiveProtorJ???',
				),
				$client->documentAttributeFilename(
					file_name : '3lkOR1tGrBDYJ8AK',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'KYatnSOXiBs7cp8y',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```