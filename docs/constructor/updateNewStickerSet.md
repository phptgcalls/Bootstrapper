# updateNewStickerSet

**Description** : *A new stickerset was installed*

**Layer** : 211

```tl
updateNewStickerSet#688a30aa stickerset:messages.StickerSet = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>stickerset</mark> | [`messages.StickerSet`](type/messages.StickerSet) | The installed stickerset |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateNewStickerSet(
	stickerset : $client->messages->stickerSet(
		set : $client->stickerSet(
			archived : true,
			official : true,
			masks : true,
			emojis : true,
			text_color : true,
			channel_emoji_status : true,
			creator : true,
			installed_date : 1,
			id : 7186818104529265962,
			access_hash : 1715636594793273228,
			title : 'FcSkPEtzAxuRZq4X',
			short_name : 'ceL0qmsItrOEYzaX',
			thumbs : array(
				$client->photoSizeEmpty(...),
				$client->photoSize(...),
				$client->photoCachedSize(...),
				$client->photoStrippedSize(...),
				$client->photoSizeProgressive(...),
				$client->photoPathSize(...),
			),
			thumb_dc_id : 13,
			thumb_version : 74,
			thumb_document_id : -7440111299132977185,
			count : 65,
			hash : 59,
		),
		packs : array(
			$client->stickerPack(
				emoticon : 'wMyKeVs5c3EpBWfh',
				documents : array(-8241038235828250514),
			),
		),
		keywords : array(
			$client->stickerKeyword(
				document_id : 9134282703504105598,
				keyword : array('XIer3E5yxFiUhgQK'),
			),
		),
		documents : array(
			$client->documentEmpty(
				id : 6350864522138945386,
			),
			$client->document(
				id : 2451552052551157487,
				access_hash : 7570728247978514756,
				file_reference : '&*?#?LiveProtoJ????',
				date : 52,
				mime_type : 'EgLFMNydaierSAot',
				size : -5260893509615857899,
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
				dc_id : 66,
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
);
```