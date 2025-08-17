# inputInvoicePremiumGiftStars

**Layer** : 211

```tl
inputInvoicePremiumGiftStars#dabab2ef flags:# user_id:InputUser months:int message:flags.0?TextWithEntities = InputInvoice;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| <mark>user_id</mark> | [`InputUser`](type/InputUser) | NOTHING |
| <mark>months</mark> | [`int`](type/int) | NOTHING |
| **message** | [`flags.0?TextWithEntities`](type/TextWithEntities) | NOTHING |

---

## Type

[InputInvoice](type/InputInvoice)

---

## Example

```php
$inputInvoice = $client->inputInvoicePremiumGiftStars(
	user_id : $client->inputUserEmpty(),
	months : 19,
	message : $client->textWithEntities(
		text : '9xrM2FW8jaSVY1Qi',
		entities : array(
			$client->messageEntityUnknown(
				offset : 56,
				length : 74,
			),
			$client->messageEntityMention(
				offset : 90,
				length : 88,
			),
			$client->messageEntityHashtag(
				offset : 5,
				length : 65,
			),
			$client->messageEntityBotCommand(
				offset : 52,
				length : 3,
			),
			$client->messageEntityUrl(
				offset : 57,
				length : 43,
			),
			$client->messageEntityEmail(
				offset : 4,
				length : 20,
			),
			$client->messageEntityBold(
				offset : 55,
				length : 51,
			),
			$client->messageEntityItalic(
				offset : 65,
				length : 70,
			),
			$client->messageEntityCode(
				offset : 43,
				length : 8,
			),
			$client->messageEntityPre(
				offset : 21,
				length : 29,
				language : 'dI9HXeLFgKpkuBio',
			),
			$client->messageEntityTextUrl(
				offset : 66,
				length : 65,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 60,
				length : 77,
				user_id : 3320087590192477489,
			),
			$client->inputMessageEntityMentionName(
				offset : 16,
				length : 14,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 57,
				length : 85,
			),
			$client->messageEntityCashtag(
				offset : 54,
				length : 95,
			),
			$client->messageEntityUnderline(
				offset : 46,
				length : 69,
			),
			$client->messageEntityStrike(
				offset : 25,
				length : 61,
			),
			$client->messageEntityBankCard(
				offset : 38,
				length : 63,
			),
			$client->messageEntitySpoiler(
				offset : 60,
				length : 100,
			),
			$client->messageEntityCustomEmoji(
				offset : 34,
				length : 60,
				document_id : -3588731285585311695,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 74,
				length : 71,
			),
		),
	),
);
```