# stickerSetNoCovered

**Description** : *Just the stickerset information, with no previews*

**Layer** : 211

```tl
stickerSetNoCovered#77b15d1c set:StickerSet = StickerSetCovered;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>set</mark> | [`StickerSet`](type/StickerSet) | Stickerset information |

---

## Type

[StickerSetCovered](type/StickerSetCovered)

---

## Example

```php
$stickerSetCovered = $client->stickerSetNoCovered(
	set : $client->stickerSet(
		archived : true,
		official : true,
		masks : true,
		emojis : true,
		text_color : true,
		channel_emoji_status : true,
		creator : true,
		installed_date : 38,
		id : -3729348230838648316,
		access_hash : -7484509928400442918,
		title : '9KJUbcwfXtYj71mI',
		short_name : 'BDFCR6VEHdPt0k4p',
		thumbs : array(
			$client->photoSizeEmpty(
				type : 'PhXdN8DJQmU316Ig',
			),
			$client->photoSize(
				type : '5vBN3fx1dmpVejh4',
				w : 36,
				h : 62,
				size : 85,
			),
			$client->photoCachedSize(
				type : '5KVvA40gd8Y673IE',
				w : 45,
				h : 11,
				bytes : '@???LiveProto?}Dq?',
			),
			$client->photoStrippedSize(
				type : '5EjqkPcTgzUMF3yN',
				bytes : 'U\\͊LiveProtod3I?',
			),
			$client->photoSizeProgressive(
				type : 'ZQAnxDSbay20O3KL',
				w : 23,
				h : 41,
				sizes : array(99),
			),
			$client->photoPathSize(
				type : 'HoubWeBgZ9XNdCSV',
				bytes : '??Î?LiveProto??FW',
			),
		),
		thumb_dc_id : 52,
		thumb_version : 29,
		thumb_document_id : -5184055807946282363,
		count : 23,
		hash : 61,
	),
);
```