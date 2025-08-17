# messageActionStarGift

**Description** : *You received a gift, see here » for more info*

**Layer** : 211

```tl
messageActionStarGift#4717e8a4 flags:# name_hidden:flags.0?true saved:flags.2?true converted:flags.3?true upgraded:flags.5?true refunded:flags.9?true can_upgrade:flags.10?true gift:StarGift message:flags.1?TextWithEntities convert_stars:flags.4?long upgrade_msg_id:flags.5?int upgrade_stars:flags.8?long from_id:flags.11?Peer peer:flags.12?Peer saved_id:flags.12?long = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **name_hidden** | [`flags.0?true`](type/true) | If set, the name of the sender of the gift will be hidden if the destination user decides to display the gift on their profile |
| **saved** | [`flags.2?true`](type/true) | Whether this gift was added to the destination user's profile (may be toggled using payments.saveStarGift and fetched using payments.getUserStarGifts) |
| **converted** | [`flags.3?true`](type/true) | Whether this gift was converted to Telegram Stars and cannot be displayed on the profile anymore |
| **upgraded** | [`flags.5?true`](type/true) | NOTHING |
| **refunded** | [`flags.9?true`](type/true) | NOTHING |
| **can_upgrade** | [`flags.10?true`](type/true) | NOTHING |
| <mark>gift</mark> | [`StarGift`](type/StarGift) | Info about the gift |
| **message** | [`flags.1?TextWithEntities`](type/TextWithEntities) | Additional message from the sender of the gift |
| **convert_stars** | [`flags.4?long`](type/long) | The receiver of this gift may convert it to this many Telegram Stars, instead of displaying it on their profile page.convert_stars will be equal to stars only if the gift was bought using recently bought Telegram Stars, otherwise it will be less than stars |
| **upgrade_msg_id** | [`flags.5?int`](type/int) | NOTHING |
| **upgrade_stars** | [`flags.8?long`](type/long) | NOTHING |
| **from_id** | [`flags.11?Peer`](type/Peer) | NOTHING |
| **peer** | [`flags.12?Peer`](type/Peer) | NOTHING |
| **saved_id** | [`flags.12?long`](type/long) | NOTHING |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionStarGift(
	name_hidden : true,
	saved : true,
	converted : true,
	upgraded : true,
	refunded : true,
	can_upgrade : true,
	gift : $client->starGift(
		limited : true,
		sold_out : true,
		birthday : true,
		require_premium : true,
		limited_per_user : true,
		id : 7848268320772826457,
		sticker : $client->documentEmpty(
			id : -8542348749407411183,
		),
		stars : 6971757684087236012,
		availability_remains : 20,
		availability_total : 18,
		availability_resale : -7061327485223200670,
		convert_stars : -5110629795388142352,
		first_sale_date : 29,
		last_sale_date : 55,
		upgrade_stars : 7610925956123846094,
		resell_min_stars : 4829155856566817904,
		title : 'ETg6Y8xA7XcB3Uab',
		released_by : $client->peerUser(
			user_id : 1929975039187067525,
		),
		per_user_total : 88,
		per_user_remains : 12,
	),
	message : $client->textWithEntities(
		text : '3HyfECh4mbtRTXlL',
		entities : array(
			$client->messageEntityUnknown(
				offset : 46,
				length : 61,
			),
			$client->messageEntityMention(
				offset : 16,
				length : 36,
			),
			$client->messageEntityHashtag(
				offset : 70,
				length : 4,
			),
			$client->messageEntityBotCommand(
				offset : 47,
				length : 18,
			),
			$client->messageEntityUrl(
				offset : 47,
				length : 47,
			),
			$client->messageEntityEmail(
				offset : 17,
				length : 77,
			),
			$client->messageEntityBold(
				offset : 21,
				length : 73,
			),
			$client->messageEntityItalic(
				offset : 78,
				length : 60,
			),
			$client->messageEntityCode(
				offset : 1,
				length : 7,
			),
			$client->messageEntityPre(
				offset : 100,
				length : 20,
				language : 'ctYINGmJXZzqkp6U',
			),
			$client->messageEntityTextUrl(
				offset : 88,
				length : 65,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 99,
				length : 74,
				user_id : 521919075713667636,
			),
			$client->inputMessageEntityMentionName(
				offset : 18,
				length : 67,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 100,
				length : 8,
			),
			$client->messageEntityCashtag(
				offset : 74,
				length : 91,
			),
			$client->messageEntityUnderline(
				offset : 86,
				length : 11,
			),
			$client->messageEntityStrike(
				offset : 95,
				length : 47,
			),
			$client->messageEntityBankCard(
				offset : 39,
				length : 62,
			),
			$client->messageEntitySpoiler(
				offset : 54,
				length : 98,
			),
			$client->messageEntityCustomEmoji(
				offset : 94,
				length : 45,
				document_id : -3393889916881321943,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 78,
				length : 61,
			),
		),
	),
	convert_stars : -7337119909847196842,
	upgrade_msg_id : 35,
	upgrade_stars : -2797246297298456921,
	from_id : $client->peerUser(
		user_id : 6505975749771295229,
	),
	peer : $client->peerUser(
		user_id : -1362925254091093238,
	),
	saved_id : 9187525954773540708,
);
```