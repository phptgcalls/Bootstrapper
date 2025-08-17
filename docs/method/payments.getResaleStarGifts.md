# payments.getResaleStarGifts

**Layer** : 211

```tl
payments.getResaleStarGifts#7a5fa236 flags:# sort_by_price:flags.1?true sort_by_num:flags.2?true attributes_hash:flags.0?long gift_id:long attributes:flags.3?Vector<StarGiftAttributeId> offset:string limit:int = payments.ResaleStarGifts;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **sort_by_price** | [`flags.1?true`](type/true) | NOTHING |
| **sort_by_num** | [`flags.2?true`](type/true) | NOTHING |
| **attributes_hash** | [`flags.0?long`](type/long) | NOTHING |
| <mark>gift_id</mark> | [`long`](type/long) | NOTHING |
| **attributes** | [`flags.3?Vector<StarGiftAttributeId>`](type/StarGiftAttributeId) | NOTHING |
| <mark>offset</mark> | [`string`](type/string) | NOTHING |
| <mark>limit</mark> | [`int`](type/int) | NOTHING |

---

## Result

[payments.ResaleStarGifts](type/payments.ResaleStarGifts)

---

## Example

```php
$paymentsResaleStarGifts = $client->payments->getResaleStarGifts(
	sort_by_price : true,
	sort_by_num : true,
	attributes_hash : -5957672589053003433,
	gift_id : -3120840620890507992,
	attributes : array(
		$client->starGiftAttributeIdModel(
			document_id : 206620381551435113,
		),
		$client->starGiftAttributeIdPattern(
			document_id : 8470065949802723079,
		),
		$client->starGiftAttributeIdBackdrop(
			backdrop_id : 47,
		),
	),
	offset : 'pWvqI6nuAxVbR4zU',
	limit : 67,
);
```