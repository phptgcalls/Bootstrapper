# messages.allStickers

**Description** : *Info about all installed stickers*

**Layer** : 211

```tl
messages.allStickers#cdbbcebb hash:long sets:Vector<StickerSet> = messages.AllStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>sets</mark> | [`Vector<StickerSet>`](type/StickerSet) | All stickersets |

---

## Type

[messages.AllStickers](type/messages.AllStickers)

---

## Example

```php
$messagesAllStickers = $client->messages->allStickers(
	hash : -9197384294618056570,
	sets : array(
		$client->stickerSet(
			archived : true,
			official : true,
			masks : true,
			emojis : true,
			text_color : true,
			channel_emoji_status : true,
			creator : true,
			installed_date : 15,
			id : -6715331082156491462,
			access_hash : -2692715734020487191,
			title : 'Ml83tTQ1u7f6O5G0',
			short_name : 'kgHOs1db0RecqW2Y',
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'Sh5fZmKIGnJLMBwy',
				),
				$client->photoSize(
					type : 'cJAhRexO28s3pQqm',
					w : 11,
					h : 3,
					size : 85,
				),
				$client->photoCachedSize(
					type : 'S0hcr7NEP6UAOk1a',
					w : 56,
					h : 40,
					bytes : '̎??LiveProto??TWX',
				),
				$client->photoStrippedSize(
					type : 'fDKqi9zuTrompAlI',
					bytes : 'v? ?LiveProto??v',
				),
				$client->photoSizeProgressive(
					type : 'GltnvkhpjZMHmrLq',
					w : 38,
					h : 30,
					sizes : array(52),
				),
				$client->photoPathSize(
					type : 'DE9INqZgkripJdbx',
					bytes : '6??LiveProto?G?G?',
				),
			),
			thumb_dc_id : 90,
			thumb_version : 18,
			thumb_document_id : -2850581810814655428,
			count : 97,
			hash : 63,
		),
	),
);
```