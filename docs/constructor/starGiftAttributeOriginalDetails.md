# starGiftAttributeOriginalDetails

**Layer** : 211

```tl
starGiftAttributeOriginalDetails#e0bff26c flags:# sender_id:flags.0?Peer recipient_id:Peer date:int message:flags.1?TextWithEntities = StarGiftAttribute;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **sender_id** | [`flags.0?Peer`](type/Peer) | NOTHING |
| <mark>recipient_id</mark> | [`Peer`](type/Peer) | NOTHING |
| <mark>date</mark> | [`int`](type/int) | NOTHING |
| **message** | [`flags.1?TextWithEntities`](type/TextWithEntities) | NOTHING |

---

## Type

[StarGiftAttribute](type/StarGiftAttribute)

---

## Example

```php
$starGiftAttribute = $client->starGiftAttributeOriginalDetails(
	sender_id : $client->peerUser(
		user_id : -1218755769312542786,
	),
	recipient_id : $client->peerUser(
		user_id : -6885988158393357474,
	),
	date : 7,
	message : $client->textWithEntities(
		text : 'ldqpvCt3BWIk0VEH',
		entities : array(
			$client->messageEntityUnknown(
				offset : 82,
				length : 47,
			),
			$client->messageEntityMention(
				offset : 2,
				length : 76,
			),
			$client->messageEntityHashtag(
				offset : 85,
				length : 64,
			),
			$client->messageEntityBotCommand(
				offset : 38,
				length : 56,
			),
			$client->messageEntityUrl(
				offset : 53,
				length : 58,
			),
			$client->messageEntityEmail(
				offset : 1,
				length : 9,
			),
			$client->messageEntityBold(
				offset : 82,
				length : 66,
			),
			$client->messageEntityItalic(
				offset : 13,
				length : 95,
			),
			$client->messageEntityCode(
				offset : 53,
				length : 65,
			),
			$client->messageEntityPre(
				offset : 14,
				length : 69,
				language : '2FMNabARSc0PxYQB',
			),
			$client->messageEntityTextUrl(
				offset : 10,
				length : 22,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 19,
				length : 86,
				user_id : 604619832752040390,
			),
			$client->inputMessageEntityMentionName(
				offset : 50,
				length : 64,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 22,
				length : 15,
			),
			$client->messageEntityCashtag(
				offset : 63,
				length : 33,
			),
			$client->messageEntityUnderline(
				offset : 45,
				length : 73,
			),
			$client->messageEntityStrike(
				offset : 3,
				length : 20,
			),
			$client->messageEntityBankCard(
				offset : 67,
				length : 55,
			),
			$client->messageEntitySpoiler(
				offset : 8,
				length : 80,
			),
			$client->messageEntityCustomEmoji(
				offset : 16,
				length : 88,
				document_id : 640143184695157558,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 28,
				length : 49,
			),
		),
	),
);
```