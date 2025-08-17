# savedStarGift

**Layer** : 211

```tl
savedStarGift#1ea646df flags:# name_hidden:flags.0?true unsaved:flags.5?true refunded:flags.9?true can_upgrade:flags.10?true pinned_to_top:flags.12?true from_id:flags.1?Peer date:int gift:StarGift message:flags.2?TextWithEntities msg_id:flags.3?int saved_id:flags.11?long convert_stars:flags.4?long upgrade_stars:flags.6?long can_export_at:flags.7?int transfer_stars:flags.8?long can_transfer_at:flags.13?int can_resell_at:flags.14?int collection_id:flags.15?Vector<int> = SavedStarGift;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **name_hidden** | [`flags.0?true`](type/true) | NOTHING |
| **unsaved** | [`flags.5?true`](type/true) | NOTHING |
| **refunded** | [`flags.9?true`](type/true) | NOTHING |
| **can_upgrade** | [`flags.10?true`](type/true) | NOTHING |
| **pinned_to_top** | [`flags.12?true`](type/true) | NOTHING |
| **from_id** | [`flags.1?Peer`](type/Peer) | NOTHING |
| <mark>date</mark> | [`int`](type/int) | NOTHING |
| <mark>gift</mark> | [`StarGift`](type/StarGift) | NOTHING |
| **message** | [`flags.2?TextWithEntities`](type/TextWithEntities) | NOTHING |
| **msg_id** | [`flags.3?int`](type/int) | NOTHING |
| **saved_id** | [`flags.11?long`](type/long) | NOTHING |
| **convert_stars** | [`flags.4?long`](type/long) | NOTHING |
| **upgrade_stars** | [`flags.6?long`](type/long) | NOTHING |
| **can_export_at** | [`flags.7?int`](type/int) | NOTHING |
| **transfer_stars** | [`flags.8?long`](type/long) | NOTHING |
| **can_transfer_at** | [`flags.13?int`](type/int) | NOTHING |
| **can_resell_at** | [`flags.14?int`](type/int) | NOTHING |
| **collection_id** | [`flags.15?Vector<int>`](type/int) | NOTHING |

---

## Type

[SavedStarGift](type/SavedStarGift)

---

## Example

```php
$savedStarGift = $client->savedStarGift(
	name_hidden : true,
	unsaved : true,
	refunded : true,
	can_upgrade : true,
	pinned_to_top : true,
	from_id : $client->peerUser(
		user_id : 5022676245330735520,
	),
	date : 35,
	gift : $client->starGift(
		limited : true,
		sold_out : true,
		birthday : true,
		require_premium : true,
		limited_per_user : true,
		id : 6590004253132815640,
		sticker : $client->documentEmpty(
			id : -8178981337035293158,
		),
		stars : -740844916491575615,
		availability_remains : 88,
		availability_total : 5,
		availability_resale : -6454226864396164693,
		convert_stars : 5276786178612431376,
		first_sale_date : 44,
		last_sale_date : 53,
		upgrade_stars : -6735918595364655766,
		resell_min_stars : -6987345328387347587,
		title : 'ZatPzR36CybUFGoi',
		released_by : $client->peerUser(
			user_id : 8112345046039204084,
		),
		per_user_total : 92,
		per_user_remains : 94,
	),
	message : $client->textWithEntities(
		text : 'bGLx7BWHwIXa8Uoc',
		entities : array(
			$client->messageEntityUnknown(
				offset : 32,
				length : 25,
			),
			$client->messageEntityMention(
				offset : 42,
				length : 56,
			),
			$client->messageEntityHashtag(
				offset : 98,
				length : 44,
			),
			$client->messageEntityBotCommand(
				offset : 95,
				length : 34,
			),
			$client->messageEntityUrl(
				offset : 1,
				length : 39,
			),
			$client->messageEntityEmail(
				offset : 77,
				length : 93,
			),
			$client->messageEntityBold(
				offset : 95,
				length : 11,
			),
			$client->messageEntityItalic(
				offset : 76,
				length : 46,
			),
			$client->messageEntityCode(
				offset : 67,
				length : 69,
			),
			$client->messageEntityPre(
				offset : 28,
				length : 13,
				language : 'SrPiYxpTI1HqNA3o',
			),
			$client->messageEntityTextUrl(
				offset : 53,
				length : 78,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 49,
				length : 62,
				user_id : -2276505640240428528,
			),
			$client->inputMessageEntityMentionName(
				offset : 51,
				length : 14,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 94,
				length : 82,
			),
			$client->messageEntityCashtag(
				offset : 8,
				length : 12,
			),
			$client->messageEntityUnderline(
				offset : 10,
				length : 30,
			),
			$client->messageEntityStrike(
				offset : 1,
				length : 48,
			),
			$client->messageEntityBankCard(
				offset : 18,
				length : 17,
			),
			$client->messageEntitySpoiler(
				offset : 27,
				length : 64,
			),
			$client->messageEntityCustomEmoji(
				offset : 47,
				length : 12,
				document_id : -1561965198919854845,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 74,
				length : 81,
			),
		),
	),
	msg_id : 77,
	saved_id : -3989081599112913769,
	convert_stars : 7159687924599853126,
	upgrade_stars : -7295419163930129332,
	can_export_at : 76,
	transfer_stars : 7285926261319327361,
	can_transfer_at : 38,
	can_resell_at : 8,
	collection_id : array(15),
);
```