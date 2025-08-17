# messages.stickerSetInstallResultArchive

**Description** : *The stickerset was installed, but since there are too many stickersets some were archived*

**Layer** : 211

```tl
messages.stickerSetInstallResultArchive#35e410a8 sets:Vector<StickerSetCovered> = messages.StickerSetInstallResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>sets</mark> | [`Vector<StickerSetCovered>`](type/StickerSetCovered) | Archived stickersets |

---

## Type

[messages.StickerSetInstallResult](type/messages.StickerSetInstallResult)

---

## Example

```php
$messagesStickerSetInstallResult = $client->messages->stickerSetInstallResultArchive(
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
				installed_date : 39,
				id : -6295954347841322171,
				access_hash : -1366114193490721150,
				title : 'djrC8GMUZtYxkJ2D',
				short_name : 'hkvWjRnPMLcdTAQ0',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 95,
				thumb_version : 96,
				thumb_document_id : -3302186685350989540,
				count : 3,
				hash : 1,
			),
			cover : $client->documentEmpty(
				id : 3731666175803631834,
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
				installed_date : 21,
				id : -1667337737095051743,
				access_hash : -7855258839703760957,
				title : 'ah6CedDMOQu1Yy5N',
				short_name : 'sk1rLMWhxJbqRv5G',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 58,
				thumb_version : 15,
				thumb_document_id : -2014844819559120230,
				count : 79,
				hash : 93,
			),
			covers : array(
				$client->documentEmpty(
					id : -7361289417237024830,
				),
				$client->document(
					id : 5293547650744239986,
					access_hash : 8715802746702299326,
					file_reference : '?vMDLiveProto?g?`?',
					date : 43,
					mime_type : '4pNvVbOWGAr3dwIx',
					size : -8335156193859175843,
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
					dc_id : 8,
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
				installed_date : 29,
				id : -8298146941959970787,
				access_hash : 5810492573185078630,
				title : 'WqkE8DmsYR62Crfc',
				short_name : 'e4Qaz6AH83dJWGnO',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 44,
				thumb_version : 70,
				thumb_document_id : 8992924092821267757,
				count : 7,
				hash : 83,
			),
			packs : array(
				$client->stickerPack(
					emoticon : 'aXSyYDBv5ENA8Fwp',
					documents : array(-5402136244056463138),
				),
			),
			keywords : array(
				$client->stickerKeyword(
					document_id : 7934100885266278403,
					keyword : array('8mtaW6fukZcSDYBe'),
				),
			),
			documents : array(
				$client->documentEmpty(
					id : -4029656201928541140,
				),
				$client->document(
					id : 8444530734770163011,
					access_hash : -1202451118157280844,
					file_reference : 'p???LiveProto~?' . "\0" . '??',
					date : 100,
					mime_type : 'P7CoLDJm4ycM9xuY',
					size : -5437498836718587845,
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
					dc_id : 2,
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
				installed_date : 58,
				id : -330936410563322691,
				access_hash : 2382040501537796084,
				title : 'VfDRtFzhI0sq2N8y',
				short_name : 'WP9GNpIVCR1uy6Zq',
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				thumb_dc_id : 71,
				thumb_version : 13,
				thumb_document_id : -7597572302661139435,
				count : 79,
				hash : 3,
			),
		),
	),
);
```