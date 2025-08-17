# messageActionGiftCode

**Description** : *Contains a Telegram Premium giftcode link*

**Layer** : 211

```tl
messageActionGiftCode#56d03994 flags:# via_giveaway:flags.0?true unclaimed:flags.5?true boost_peer:flags.1?Peer months:int slug:string currency:flags.2?string amount:flags.2?long crypto_currency:flags.3?string crypto_amount:flags.3?long message:flags.4?TextWithEntities = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **via_giveaway** | [`flags.0?true`](type/true) | If set, this gift code was received from a giveaway » started by a channel/supergroup we're subscribed to |
| **unclaimed** | [`flags.5?true`](type/true) | If set, the link was not redeemed yet |
| **boost_peer** | [`flags.1?Peer`](type/Peer) | Identifier of the channel/supergroup that created the gift code either directly or through a giveaway: if we import this giftcode link, we will also automatically boost this channel/supergroup |
| <mark>months</mark> | [`int`](type/int) | Duration in months of the gifted Telegram Premium subscription |
| <mark>slug</mark> | [`string`](type/string) | Slug of the Telegram Premium giftcode link |
| **currency** | [`flags.2?string`](type/string) | Three-letter ISO 4217 currency code |
| **amount** | [`flags.2?long`](type/long) | Total price in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |
| **crypto_currency** | [`flags.3?string`](type/string) | If set, the gift was made using the specified cryptocurrency |
| **crypto_amount** | [`flags.3?long`](type/long) | If crypto_currency is set, contains the paid amount, in the smallest units of the cryptocurrency |
| **message** | [`flags.4?TextWithEntities`](type/TextWithEntities) | Message attached with the gift |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionGiftCode(
	via_giveaway : true,
	unclaimed : true,
	boost_peer : $client->peerUser(
		user_id : -1242845739085451693,
	),
	months : 42,
	slug : 'OpSQahuUzL3gDt6c',
	currency : 'yPvNzY1C9Jd6VFj8',
	amount : -2279203977432667906,
	crypto_currency : 'Ij51OYcyf39iuMGn',
	crypto_amount : -8937922375256536667,
	message : $client->textWithEntities(
		text : 'bsPoIO1ZtXg5veND',
		entities : array(
			$client->messageEntityUnknown(
				offset : 91,
				length : 57,
			),
			$client->messageEntityMention(
				offset : 30,
				length : 10,
			),
			$client->messageEntityHashtag(
				offset : 39,
				length : 53,
			),
			$client->messageEntityBotCommand(
				offset : 39,
				length : 28,
			),
			$client->messageEntityUrl(
				offset : 12,
				length : 60,
			),
			$client->messageEntityEmail(
				offset : 22,
				length : 68,
			),
			$client->messageEntityBold(
				offset : 66,
				length : 61,
			),
			$client->messageEntityItalic(
				offset : 22,
				length : 51,
			),
			$client->messageEntityCode(
				offset : 53,
				length : 95,
			),
			$client->messageEntityPre(
				offset : 38,
				length : 55,
				language : 'LfyQi9ZuocOvR6aw',
			),
			$client->messageEntityTextUrl(
				offset : 92,
				length : 43,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 74,
				length : 16,
				user_id : 5945564074361813893,
			),
			$client->inputMessageEntityMentionName(
				offset : 87,
				length : 31,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 7,
				length : 18,
			),
			$client->messageEntityCashtag(
				offset : 24,
				length : 65,
			),
			$client->messageEntityUnderline(
				offset : 40,
				length : 12,
			),
			$client->messageEntityStrike(
				offset : 30,
				length : 21,
			),
			$client->messageEntityBankCard(
				offset : 31,
				length : 74,
			),
			$client->messageEntitySpoiler(
				offset : 97,
				length : 63,
			),
			$client->messageEntityCustomEmoji(
				offset : 66,
				length : 16,
				document_id : -9027466382606892947,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 33,
				length : 44,
			),
		),
	),
);
```