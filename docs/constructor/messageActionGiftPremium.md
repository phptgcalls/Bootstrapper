# messageActionGiftPremium

**Description** : *Info about a gifted Telegram Premium subscription*

**Layer** : 211

```tl
messageActionGiftPremium#6c6274fa flags:# currency:string amount:long months:int crypto_currency:flags.0?string crypto_amount:flags.0?long message:flags.1?TextWithEntities = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code |
| <mark>amount</mark> | [`long`](type/long) | Price of the gift in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |
| <mark>months</mark> | [`int`](type/int) | Duration of the gifted Telegram Premium subscription |
| **crypto_currency** | [`flags.0?string`](type/string) | If the gift was bought using a cryptocurrency, the cryptocurrency name |
| **crypto_amount** | [`flags.0?long`](type/long) | If the gift was bought using a cryptocurrency, price of the gift in the smallest units of a cryptocurrency |
| **message** | [`flags.1?TextWithEntities`](type/TextWithEntities) | Message attached with the gift |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionGiftPremium(
	currency : 'sPRyKwX3zcDnk8UL',
	amount : -8229897456476332049,
	months : 54,
	crypto_currency : 'O43FYZ6DUSnhmxcq',
	crypto_amount : -1744895988746354468,
	message : $client->textWithEntities(
		text : 'CRdNp7Dm5LwKzQEy',
		entities : array(
			$client->messageEntityUnknown(
				offset : 1,
				length : 9,
			),
			$client->messageEntityMention(
				offset : 8,
				length : 93,
			),
			$client->messageEntityHashtag(
				offset : 78,
				length : 35,
			),
			$client->messageEntityBotCommand(
				offset : 23,
				length : 68,
			),
			$client->messageEntityUrl(
				offset : 10,
				length : 22,
			),
			$client->messageEntityEmail(
				offset : 44,
				length : 78,
			),
			$client->messageEntityBold(
				offset : 68,
				length : 59,
			),
			$client->messageEntityItalic(
				offset : 21,
				length : 88,
			),
			$client->messageEntityCode(
				offset : 90,
				length : 28,
			),
			$client->messageEntityPre(
				offset : 51,
				length : 77,
				language : 'chT7QBkKIFrjNwUR',
			),
			$client->messageEntityTextUrl(
				offset : 83,
				length : 41,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 68,
				length : 28,
				user_id : 6129709301445314403,
			),
			$client->inputMessageEntityMentionName(
				offset : 61,
				length : 22,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 45,
				length : 47,
			),
			$client->messageEntityCashtag(
				offset : 13,
				length : 47,
			),
			$client->messageEntityUnderline(
				offset : 15,
				length : 36,
			),
			$client->messageEntityStrike(
				offset : 60,
				length : 47,
			),
			$client->messageEntityBankCard(
				offset : 35,
				length : 8,
			),
			$client->messageEntitySpoiler(
				offset : 1,
				length : 50,
			),
			$client->messageEntityCustomEmoji(
				offset : 54,
				length : 88,
				document_id : 7236973655995067216,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 97,
				length : 20,
			),
		),
	),
);
```