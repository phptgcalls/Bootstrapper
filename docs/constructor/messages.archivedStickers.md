# messages.archivedStickers

**Description** : *Archived stickersets*

**Layer** : 211

```tl
messages.archivedStickers#4fcba9c8 count:int sets:Vector<StickerSetCovered> = messages.ArchivedStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Number of archived stickers |
| <mark>sets</mark> | [`Vector<StickerSetCovered>`](type/StickerSetCovered) | Archived stickersets |

---

## Type

[messages.ArchivedStickers](type/messages.ArchivedStickers)

---

## Example

```php
$messagesArchivedStickers = $client->messages->archivedStickers(
	count : 55,
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
				installed_date : 18,
				id : 4157223169683568664,
				access_hash : 3702722174404889783,
				title : 'Lm9IBcW8ykjSRZue',
				short_name : '5JeEH9qbBnTc48Xx',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 15,
				thumb_version : 75,
				thumb_document_id : -4049979888543362396,
				count : 4,
				hash : 90,
			),
			cover : $client->documentEmpty(
				id : -8064546786603435916,
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
				installed_date : 73,
				id : -8620629722930867501,
				access_hash : -400195778234821460,
				title : 'wbqIcxAndmR8QoJa',
				short_name : 'PQcKFUj5oZ67zNXb',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 87,
				thumb_version : 60,
				thumb_document_id : 7344679203178979559,
				count : 26,
				hash : 29,
			),
			covers : array(
				$client->documentEmpty(
					id : -6507350325989516681,
				),
				$client->document(
					id : 1148492294055186112,
					access_hash : -8698022744332291867,
					file_reference : '??JN?LiveProto??c??',
					date : 81,
					mime_type : 'HxpvQz5fUWG8clFh',
					size : -5444069959185616190,
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
					dc_id : 49,
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
				installed_date : 17,
				id : 3609342490208581109,
				access_hash : 5236281039986072915,
				title : 'QEeRkDH72IfZW9NK',
				short_name : 'cFU6tfAXnkGSJpdg',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 61,
				thumb_version : 0,
				thumb_document_id : 6125485949009052828,
				count : 72,
				hash : 99,
			),
			packs : array(
				$client->stickerPack(
					emoticon : 'pE6zudieOR9Abnx8',
					documents : array(-4144549775281762762),
				),
			),
			keywords : array(
				$client->stickerKeyword(
					document_id : -2228012249739698909,
					keyword : array('NGclpQam4DzVnxb2'),
				),
			),
			documents : array(
				$client->documentEmpty(
					id : -4331919696671688903,
				),
				$client->document(
					id : -3596776183519188646,
					access_hash : -3307814955393155742,
					file_reference : '1?K??LiveProto?Yw? ',
					date : 25,
					mime_type : 'XWIY6mkHA7SoPMTD',
					size : 3037488465616808272,
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
					dc_id : 73,
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
				installed_date : 3,
				id : -255647502869942378,
				access_hash : -7484862526070187603,
				title : 'lzKVDwnmHLpyUaBW',
				short_name : 'eokLMqUTjtEAWlgs',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 57,
				thumb_version : 69,
				thumb_document_id : -2386791713052093270,
				count : 35,
				hash : 87,
			),
		),
	),
);
```