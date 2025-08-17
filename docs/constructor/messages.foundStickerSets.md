# messages.foundStickerSets

**Description** : *Found stickersets*

**Layer** : 211

```tl
messages.foundStickerSets#8af09dd2 hash:long sets:Vector<StickerSetCovered> = messages.FoundStickerSets;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>sets</mark> | [`Vector<StickerSetCovered>`](type/StickerSetCovered) | Found stickersets |

---

## Type

[messages.FoundStickerSets](type/messages.FoundStickerSets)

---

## Example

```php
$messagesFoundStickerSets = $client->messages->foundStickerSets(
	hash : 3421232238571739657,
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
				installed_date : 67,
				id : -8717765262107137411,
				access_hash : -4751928373444082214,
				title : 'AVuIeMTPR08nkz15',
				short_name : 'axhLTBMvEykKNrXC',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 75,
				thumb_version : 77,
				thumb_document_id : 7871260250187873918,
				count : 97,
				hash : 63,
			),
			cover : $client->documentEmpty(
				id : -5488223589662512209,
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
				installed_date : 39,
				id : -4859408262413265253,
				access_hash : -1253693493483559888,
				title : '7Ikn3xMTcp60SXza',
				short_name : '5WP3s2Oaj9UNzZCH',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 87,
				thumb_version : 6,
				thumb_document_id : -3215892929434438798,
				count : 90,
				hash : 28,
			),
			covers : array(
				$client->documentEmpty(
					id : 6110985986440878746,
				),
				$client->document(
					id : -7329834327727760276,
					access_hash : -1957162986537154113,
					file_reference : '?^n??LiveProto??o',
					date : 85,
					mime_type : 'N3VrjZ8W9oRFSM1Q',
					size : 8990474070048087172,
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
					dc_id : 33,
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
				installed_date : 70,
				id : -4760015460559385733,
				access_hash : 4457650383584493190,
				title : 'yVijfY8bv5ZuQSFq',
				short_name : 'pbyOjP4ZBKrmLCtd',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 87,
				thumb_version : 68,
				thumb_document_id : 8858049187462188887,
				count : 1,
				hash : 73,
			),
			packs : array(
				$client->stickerPack(
					emoticon : 'WJNyEV51SwD4dKGO',
					documents : array(-2403427169405952674),
				),
			),
			keywords : array(
				$client->stickerKeyword(
					document_id : 1008300366792064017,
					keyword : array('k0yXJHSF2obZ7Y9h'),
				),
			),
			documents : array(
				$client->documentEmpty(
					id : 4266890386154450203,
				),
				$client->document(
					id : -5440953655522277830,
					access_hash : 137776769215329718,
					file_reference : '?,LiveProto?v???',
					date : 74,
					mime_type : '84xESm7Q9Lvfe5l0',
					size : -722490648176794674,
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
					dc_id : 78,
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
				installed_date : 83,
				id : -2877616443379078838,
				access_hash : 3580278041272057103,
				title : 'KSGTBqyb5Y7rHplg',
				short_name : 'vyxDUwha8ipS3YHr',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 68,
				thumb_version : 3,
				thumb_document_id : -2165402789822953675,
				count : 0,
				hash : 52,
			),
		),
	),
);
```