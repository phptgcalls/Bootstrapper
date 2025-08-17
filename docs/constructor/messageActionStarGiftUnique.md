# messageActionStarGiftUnique

**Layer** : 211

```tl
messageActionStarGiftUnique#34f762f3 flags:# upgrade:flags.0?true transferred:flags.1?true saved:flags.2?true refunded:flags.5?true gift:StarGift can_export_at:flags.3?int transfer_stars:flags.4?long from_id:flags.6?Peer peer:flags.7?Peer saved_id:flags.7?long resale_amount:flags.8?StarsAmount can_transfer_at:flags.9?int can_resell_at:flags.10?int = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **upgrade** | [`flags.0?true`](type/true) | NOTHING |
| **transferred** | [`flags.1?true`](type/true) | NOTHING |
| **saved** | [`flags.2?true`](type/true) | NOTHING |
| **refunded** | [`flags.5?true`](type/true) | NOTHING |
| <mark>gift</mark> | [`StarGift`](type/StarGift) | NOTHING |
| **can_export_at** | [`flags.3?int`](type/int) | NOTHING |
| **transfer_stars** | [`flags.4?long`](type/long) | NOTHING |
| **from_id** | [`flags.6?Peer`](type/Peer) | NOTHING |
| **peer** | [`flags.7?Peer`](type/Peer) | NOTHING |
| **saved_id** | [`flags.7?long`](type/long) | NOTHING |
| **resale_amount** | [`flags.8?StarsAmount`](type/StarsAmount) | NOTHING |
| **can_transfer_at** | [`flags.9?int`](type/int) | NOTHING |
| **can_resell_at** | [`flags.10?int`](type/int) | NOTHING |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionStarGiftUnique(
	upgrade : true,
	transferred : true,
	saved : true,
	refunded : true,
	gift : $client->starGift(
		limited : true,
		sold_out : true,
		birthday : true,
		require_premium : true,
		limited_per_user : true,
		id : 1362884033665821411,
		sticker : $client->documentEmpty(
			id : -8351779786598083403,
		),
		stars : 8080739526655987480,
		availability_remains : 25,
		availability_total : 80,
		availability_resale : 111343438681944158,
		convert_stars : 2296917906077884767,
		first_sale_date : 99,
		last_sale_date : 26,
		upgrade_stars : -2042614250388982698,
		resell_min_stars : 237441811967308090,
		title : 'fhGVBqdAg0Mlazi2',
		released_by : $client->peerUser(
			user_id : -4817756513467108529,
		),
		per_user_total : 85,
		per_user_remains : 69,
	),
	can_export_at : 73,
	transfer_stars : 2366175236708024940,
	from_id : $client->peerUser(
		user_id : -5821575783756116739,
	),
	peer : $client->peerUser(
		user_id : -154154232033433829,
	),
	saved_id : -1697989436498248637,
	resale_amount : $client->starsAmount(
		amount : 8188438651891412225,
		nanos : 83,
	),
	can_transfer_at : 90,
	can_resell_at : 62,
);
```