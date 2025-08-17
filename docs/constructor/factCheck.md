# factCheck

**Description** : *Represents a fact-check » created by an independent fact-checker*

**Layer** : 211

```tl
factCheck#b89bfccf flags:# need_check:flags.0?true country:flags.1?string text:flags.1?TextWithEntities hash:long = FactCheck;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **need_check** | [`flags.0?true`](type/true) | If set, the country/text fields will not be set, and the fact check must be fetched manually by the client (if it isn't already cached with the key specified in hash) using bundled messages.getFactCheck requests, when the message with the factcheck scrolls into view |
| **country** | [`flags.1?string`](type/string) | A two-letter ISO 3166-1 alpha-2 country code of the country for which the fact-check should be shown |
| **text** | [`flags.1?TextWithEntities`](type/TextWithEntities) | The fact-check |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Type

[FactCheck](type/FactCheck)

---

## Example

```php
$factCheck = $client->factCheck(
	need_check : true,
	country : 'XAegGBNOj8uSVCna',
	text : $client->textWithEntities(
		text : 'Yu1aiQFT8lx57Egs',
		entities : array(
			$client->messageEntityUnknown(
				offset : 38,
				length : 67,
			),
			$client->messageEntityMention(
				offset : 97,
				length : 11,
			),
			$client->messageEntityHashtag(
				offset : 50,
				length : 100,
			),
			$client->messageEntityBotCommand(
				offset : 65,
				length : 84,
			),
			$client->messageEntityUrl(
				offset : 32,
				length : 70,
			),
			$client->messageEntityEmail(
				offset : 89,
				length : 60,
			),
			$client->messageEntityBold(
				offset : 33,
				length : 71,
			),
			$client->messageEntityItalic(
				offset : 47,
				length : 22,
			),
			$client->messageEntityCode(
				offset : 61,
				length : 55,
			),
			$client->messageEntityPre(
				offset : 23,
				length : 84,
				language : '2VS34KCToezw6Af7',
			),
			$client->messageEntityTextUrl(
				offset : 38,
				length : 59,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 89,
				length : 1,
				user_id : -425735795126673299,
			),
			$client->inputMessageEntityMentionName(
				offset : 68,
				length : 9,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 39,
				length : 24,
			),
			$client->messageEntityCashtag(
				offset : 84,
				length : 71,
			),
			$client->messageEntityUnderline(
				offset : 92,
				length : 61,
			),
			$client->messageEntityStrike(
				offset : 43,
				length : 72,
			),
			$client->messageEntityBankCard(
				offset : 71,
				length : 0,
			),
			$client->messageEntitySpoiler(
				offset : 34,
				length : 98,
			),
			$client->messageEntityCustomEmoji(
				offset : 74,
				length : 9,
				document_id : -5020869138876281304,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 78,
				length : 77,
			),
		),
	),
	hash : -1814143415563837740,
);
```