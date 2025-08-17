# starGiftUnique

**Layer** : 211

```tl
starGiftUnique#3a274d50 flags:# require_premium:flags.6?true resale_ton_only:flags.7?true id:long title:string slug:string num:int owner_id:flags.0?Peer owner_name:flags.1?string owner_address:flags.2?string attributes:Vector<StarGiftAttribute> availability_issued:int availability_total:int gift_address:flags.3?string resell_amount:flags.4?Vector<StarsAmount> released_by:flags.5?Peer = StarGift;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **require_premium** | [`flags.6?true`](type/true) | NOTHING |
| **resale_ton_only** | [`flags.7?true`](type/true) | NOTHING |
| <mark>id</mark> | [`long`](type/long) | NOTHING |
| <mark>title</mark> | [`string`](type/string) | NOTHING |
| <mark>slug</mark> | [`string`](type/string) | NOTHING |
| <mark>num</mark> | [`int`](type/int) | NOTHING |
| **owner_id** | [`flags.0?Peer`](type/Peer) | NOTHING |
| **owner_name** | [`flags.1?string`](type/string) | NOTHING |
| **owner_address** | [`flags.2?string`](type/string) | NOTHING |
| <mark>attributes</mark> | [`Vector<StarGiftAttribute>`](type/StarGiftAttribute) | NOTHING |
| <mark>availability_issued</mark> | [`int`](type/int) | NOTHING |
| <mark>availability_total</mark> | [`int`](type/int) | NOTHING |
| **gift_address** | [`flags.3?string`](type/string) | NOTHING |
| **resell_amount** | [`flags.4?Vector<StarsAmount>`](type/StarsAmount) | NOTHING |
| **released_by** | [`flags.5?Peer`](type/Peer) | NOTHING |

---

## Type

[StarGift](type/StarGift)

---

## Example

```php
$starGift = $client->starGiftUnique(
	require_premium : true,
	resale_ton_only : true,
	id : 4124888355799509904,
	title : '6UMtzjvOaBhs9Eo4',
	slug : 'nDewFAxOsiGa6U7g',
	num : 84,
	owner_id : $client->peerUser(
		user_id : -6407423996518440375,
	),
	owner_name : 'BD7zMCmds5pfl9XY',
	owner_address : 'fb4J7gIPN6crEQpk',
	attributes : array(
		$client->starGiftAttributeModel(
			name : 'CDnfvQg0bAyuZYq4',
			document : $client->documentEmpty(
				id : -6495808635253511908,
			),
			rarity_permille : 20,
		),
		$client->starGiftAttributePattern(
			name : 'sezYBlCMAU0cofFp',
			document : $client->documentEmpty(
				id : 4911337779675983970,
			),
			rarity_permille : 8,
		),
		$client->starGiftAttributeBackdrop(
			name : 'UoKnYEX2xeAZiIqy',
			backdrop_id : 21,
			center_color : 56,
			edge_color : 54,
			pattern_color : 3,
			text_color : 87,
			rarity_permille : 9,
		),
		$client->starGiftAttributeOriginalDetails(
			sender_id : $client->peerUser(
				user_id : -5356069666208991363,
			),
			recipient_id : $client->peerUser(
				user_id : 5360817757980475703,
			),
			date : 81,
			message : $client->textWithEntities(
				text : 'eCzpmOdN2lYSURDt',
				entities : array(
					$client->messageEntityUnknown(...),
					$client->messageEntityMention(...),
					$client->messageEntityHashtag(...),
					$client->messageEntityBotCommand(...),
					$client->messageEntityUrl(...),
					$client->messageEntityEmail(...),
					$client->messageEntityBold(...),
					$client->messageEntityItalic(...),
					$client->messageEntityCode(...),
					$client->messageEntityPre(...),
					$client->messageEntityTextUrl(...),
					$client->messageEntityMentionName(...),
					$client->inputMessageEntityMentionName(...),
					$client->messageEntityPhone(...),
					$client->messageEntityCashtag(...),
					$client->messageEntityUnderline(...),
					$client->messageEntityStrike(...),
					$client->messageEntityBankCard(...),
					$client->messageEntitySpoiler(...),
					$client->messageEntityCustomEmoji(...),
					$client->messageEntityBlockquote(...),
				),
			),
		),
	),
	availability_issued : 3,
	availability_total : 79,
	gift_address : 'Q57UhsrCBzLu6oa0',
	resell_amount : array(
		$client->starsAmount(
			amount : 763208871441346031,
			nanos : 77,
		),
		$client->starsTonAmount(
			amount : -3255188712105480297,
		),
	),
	released_by : $client->peerUser(
		user_id : 1492878153525792359,
	),
);
```