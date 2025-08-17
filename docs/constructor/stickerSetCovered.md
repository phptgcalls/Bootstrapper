# stickerSetCovered

**Description** : *Stickerset with a single sticker as preview*

**Layer** : 211

```tl
stickerSetCovered#6410a5d2 set:StickerSet cover:Document = StickerSetCovered;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>set</mark> | [`StickerSet`](type/StickerSet) | Stickerset |
| <mark>cover</mark> | [`Document`](type/Document) | Preview |

---

## Type

[StickerSetCovered](type/StickerSetCovered)

---

## Example

```php
$stickerSetCovered = $client->stickerSetCovered(
	set : $client->stickerSet(
		archived : true,
		official : true,
		masks : true,
		emojis : true,
		text_color : true,
		channel_emoji_status : true,
		creator : true,
		installed_date : 30,
		id : -8199888651348181336,
		access_hash : 2192084479733787575,
		title : 'MabrNCziL6FowtAl',
		short_name : '0tQcECuTdNrVKlZJ',
		thumbs : array(
			$client->photoSizeEmpty(
				type : 'voy8p3AZLiQJIelb',
			),
			$client->photoSize(
				type : 'CQg6yAlb3f7kwKRG',
				w : 82,
				h : 16,
				size : 51,
			),
			$client->photoCachedSize(
				type : 'oLtd1qgFOCb3SkMj',
				w : 6,
				h : 62,
				bytes : '?sr5hLiveProto?=?;',
			),
			$client->photoStrippedSize(
				type : 'UwgdAzqM5bH3Gn1D',
				bytes : '??℗LiveProto?q???',
			),
			$client->photoSizeProgressive(
				type : 'IkTRjMmw2PpzxnaZ',
				w : 42,
				h : 91,
				sizes : array(60),
			),
			$client->photoPathSize(
				type : 'fPO9ZLE1GNiAIYRk',
				bytes : '??:e?LiveProto?N?%#',
			),
		),
		thumb_dc_id : 72,
		thumb_version : 26,
		thumb_document_id : 1386178139416317639,
		count : 64,
		hash : 75,
	),
	cover : $client->documentEmpty(
		id : 4274421462647248306,
	),
);
```