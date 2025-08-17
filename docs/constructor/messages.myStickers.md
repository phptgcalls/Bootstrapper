# messages.myStickers

**Description** : *The list of stickersets owned by the current account »*

**Layer** : 211

```tl
messages.myStickers#faff629d count:int sets:Vector<StickerSetCovered> = messages.MyStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Total number of owned stickersets |
| <mark>sets</mark> | [`Vector<StickerSetCovered>`](type/StickerSetCovered) | Stickersets |

---

## Type

[messages.MyStickers](type/messages.MyStickers)

---

## Example

```php
$messagesMyStickers = $client->messages->myStickers(
	count : 81,
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
				installed_date : 66,
				id : 6358837527129857890,
				access_hash : 7000983658220129582,
				title : 'yNTpcmFI523AZCgM',
				short_name : 'zJTOdw2IoDisqPpY',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 74,
				thumb_version : 89,
				thumb_document_id : 820405543672198908,
				count : 84,
				hash : 23,
			),
			cover : $client->documentEmpty(
				id : -2555045620677423399,
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
				installed_date : 82,
				id : -1681748751945696318,
				access_hash : 1557157128213320598,
				title : 'kTc0qJIRwBgm62xM',
				short_name : 'IWx3ePJkgf68SaOr',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 44,
				thumb_version : 0,
				thumb_document_id : -3215302464712308028,
				count : 72,
				hash : 96,
			),
			covers : array(
				$client->documentEmpty(
					id : -6208521355958587963,
				),
				$client->document(
					id : -7742301505548780827,
					access_hash : -3020495802799939241,
					file_reference : '???^LiveProto??N?.',
					date : 68,
					mime_type : 'ncJ3Sjr1feokENui',
					size : -4859901224154061319,
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
					dc_id : 75,
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
				installed_date : 53,
				id : -7117476231230701987,
				access_hash : -3226185329926553772,
				title : 'VQU0ZugH3DCW6oj5',
				short_name : 'QULAkEcpqVbho2a8',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 45,
				thumb_version : 7,
				thumb_document_id : 1612376231647967781,
				count : 7,
				hash : 46,
			),
			packs : array(
				$client->stickerPack(
					emoticon : '64jNfIeG8Y9k1wQJ',
					documents : array(-8552665425444957860),
				),
			),
			keywords : array(
				$client->stickerKeyword(
					document_id : 1801503290268681564,
					keyword : array('hbwDjsxeG8uiodM5'),
				),
			),
			documents : array(
				$client->documentEmpty(
					id : 5885077503772115203,
				),
				$client->document(
					id : -326882148996431023,
					access_hash : 6438894644511491682,
					file_reference : '??*?LiveProto??A<<',
					date : 73,
					mime_type : '7i8CEfjnAIv3wkBx',
					size : -2983075380530666358,
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
					dc_id : 9,
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
				installed_date : 1,
				id : 673026978864973067,
				access_hash : 640578832267302898,
				title : 'zcrekfdthWFbD4A6',
				short_name : 'T0iLCGHFs1cQAtEd',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 41,
				thumb_version : 36,
				thumb_document_id : 8803046521030848711,
				count : 57,
				hash : 13,
			),
		),
	),
);
```