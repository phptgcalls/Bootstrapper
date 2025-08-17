# messages.featuredStickers

**Description** : *Featured stickersets*

**Layer** : 211

```tl
messages.featuredStickers#be382906 flags:# premium:flags.0?true hash:long count:int sets:Vector<StickerSetCovered> unread:Vector<long> = messages.FeaturedStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **premium** | [`flags.0?true`](type/true) | Whether this is a premium stickerset |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>count</mark> | [`int`](type/int) | Total number of featured stickers |
| <mark>sets</mark> | [`Vector<StickerSetCovered>`](type/StickerSetCovered) | Featured stickersets |
| <mark>unread</mark> | [`Vector<long>`](type/long) | IDs of new featured stickersets |

---

## Type

[messages.FeaturedStickers](type/messages.FeaturedStickers)

---

## Example

```php
$messagesFeaturedStickers = $client->messages->featuredStickers(
	premium : true,
	hash : -5823062411756959302,
	count : 41,
	sets : array(
		$client->stickerSetCovered(
			set : $client->stickerSet(
				archived : true,
				official : true,
				masks : true,
				emojis : true,
				text_color : true,
				channel_emoji_status : true,
				creator : true,
				installed_date : 34,
				id : -780442755184767963,
				access_hash : 7370977699180041680,
				title : 'aZ2yDS7LUX0tpoqK',
				short_name : 'jyS1XpM0bCWNqePf',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 13,
				thumb_version : 31,
				thumb_document_id : 5479945282169175734,
				count : 2,
				hash : 70,
			),
			cover : $client->documentEmpty(
				id : -3265163198402534868,
			),
		),
		$client->stickerSetMultiCovered(
			set : $client->stickerSet(
				archived : true,
				official : true,
				masks : true,
				emojis : true,
				text_color : true,
				channel_emoji_status : true,
				creator : true,
				installed_date : 41,
				id : -468005352492722640,
				access_hash : 5288034913007346053,
				title : 'SephdY71WTwDJEMK',
				short_name : 'dciVAn3upoZKmP1y',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 11,
				thumb_version : 12,
				thumb_document_id : 3313251467947471709,
				count : 61,
				hash : 92,
			),
			covers : array(
				$client->documentEmpty(
					id : -2813228896682416399,
				),
				$client->document(
					id : -6369039271463388265,
					access_hash : -3953916681033767501,
					file_reference : '??HKoLiveProto.\\?i',
					date : 27,
					mime_type : 'iJuth1Kk4mgG0vnp',
					size : 7673971799152947185,
					thumbs : array(
						$client->photoSizeEmpty(...),
						$client->photoSize(...),
						$client->photoCachedSize(...),
						$client->photoStrippedSize(...),
						$client->photoSizeProgressive(...),
						$client->photoPathSize(...),
					),
					video_thumbs : array(
						$client->videoSize(...),
						$client->videoSizeEmojiMarkup(...),
						$client->videoSizeStickerMarkup(...),
					),
					dc_id : 64,
					attributes : array(
						$client->documentAttributeImageSize(...),
						$client->documentAttributeAnimated(...),
						$client->documentAttributeSticker(...),
						$client->documentAttributeVideo(...),
						$client->documentAttributeAudio(...),
						$client->documentAttributeFilename(...),
						$client->documentAttributeHasStickers(...),
						$client->documentAttributeCustomEmoji(...),
					),
				),
			),
		),
		$client->stickerSetFullCovered(
			set : $client->stickerSet(
				archived : true,
				official : true,
				masks : true,
				emojis : true,
				text_color : true,
				channel_emoji_status : true,
				creator : true,
				installed_date : 39,
				id : 6047630294537416321,
				access_hash : -7304266392912229960,
				title : '7tMfkiU2BHd6a8AG',
				short_name : 'WEihA70BjHZpnu4R',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 85,
				thumb_version : 98,
				thumb_document_id : 2702011565587344077,
				count : 91,
				hash : 60,
			),
			packs : array(
				$client->stickerPack(
					emoticon : 'BotedYlczam0gqSP',
					documents : array(9125815871450093330),
				),
			),
			keywords : array(
				$client->stickerKeyword(
					document_id : 5716085984673231661,
					keyword : array('TWtrnCZl83pmPeKO'),
				),
			),
			documents : array(
				$client->documentEmpty(
					id : -5825972445556359749,
				),
				$client->document(
					id : -3639865619024910511,
					access_hash : 346639554102067931,
					file_reference : '??<??LiveProtoO?΢
',
					date : 39,
					mime_type : 'A9zvHj4iXBwxcYkO',
					size : 347125534365075656,
					thumbs : array(
						$client->photoSizeEmpty(...),
						$client->photoSize(...),
						$client->photoCachedSize(...),
						$client->photoStrippedSize(...),
						$client->photoSizeProgressive(...),
						$client->photoPathSize(...),
					),
					video_thumbs : array(
						$client->videoSize(...),
						$client->videoSizeEmojiMarkup(...),
						$client->videoSizeStickerMarkup(...),
					),
					dc_id : 88,
					attributes : array(
						$client->documentAttributeImageSize(...),
						$client->documentAttributeAnimated(...),
						$client->documentAttributeSticker(...),
						$client->documentAttributeVideo(...),
						$client->documentAttributeAudio(...),
						$client->documentAttributeFilename(...),
						$client->documentAttributeHasStickers(...),
						$client->documentAttributeCustomEmoji(...),
					),
				),
			),
		),
		$client->stickerSetNoCovered(
			set : $client->stickerSet(
				archived : true,
				official : true,
				masks : true,
				emojis : true,
				text_color : true,
				channel_emoji_status : true,
				creator : true,
				installed_date : 73,
				id : 456673230565457298,
				access_hash : -1649722606282699582,
				title : 'QMJ5P7sxGiz3W2gm',
				short_name : '1eNBtZGKjskgyo0n',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 60,
				thumb_version : 50,
				thumb_document_id : -1178112519812612594,
				count : 88,
				hash : 58,
			),
		),
	),
	unread : array(-1754145167087515327),
);
```