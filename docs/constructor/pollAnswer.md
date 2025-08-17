# pollAnswer

**Description** : *A possible answer of a poll*

**Layer** : 211

```tl
pollAnswer#ff16e2ca text:TextWithEntities option:bytes = PollAnswer;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>text</mark> | [`TextWithEntities`](type/TextWithEntities) | Textual representation of the answer (only Premium users can use custom emoji entities here) |
| <mark>option</mark> | [`bytes`](type/bytes) | The param that has to be passed to messages.sendVote |

---

## Type

[PollAnswer](type/PollAnswer)

---

## Example

```php
$pollAnswer = $client->pollAnswer(
	text : $client->textWithEntities(
		text : 'FbPOoAm4uhtGKQ3J',
		entities : array(
			$client->messageEntityUnknown(
				offset : 3,
				length : 37,
			),
			$client->messageEntityMention(
				offset : 45,
				length : 15,
			),
			$client->messageEntityHashtag(
				offset : 68,
				length : 80,
			),
			$client->messageEntityBotCommand(
				offset : 8,
				length : 54,
			),
			$client->messageEntityUrl(
				offset : 29,
				length : 86,
			),
			$client->messageEntityEmail(
				offset : 31,
				length : 72,
			),
			$client->messageEntityBold(
				offset : 65,
				length : 52,
			),
			$client->messageEntityItalic(
				offset : 25,
				length : 14,
			),
			$client->messageEntityCode(
				offset : 62,
				length : 66,
			),
			$client->messageEntityPre(
				offset : 99,
				length : 66,
				language : 'C9VmMD8RHL3BfYx4',
			),
			$client->messageEntityTextUrl(
				offset : 74,
				length : 17,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 27,
				length : 83,
				user_id : 8275369749820485365,
			),
			$client->inputMessageEntityMentionName(
				offset : 21,
				length : 87,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 18,
				length : 6,
			),
			$client->messageEntityCashtag(
				offset : 78,
				length : 40,
			),
			$client->messageEntityUnderline(
				offset : 36,
				length : 91,
			),
			$client->messageEntityStrike(
				offset : 29,
				length : 43,
			),
			$client->messageEntityBankCard(
				offset : 13,
				length : 55,
			),
			$client->messageEntitySpoiler(
				offset : 39,
				length : 77,
			),
			$client->messageEntityCustomEmoji(
				offset : 14,
				length : 65,
				document_id : -6195056537465510031,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 81,
				length : 97,
			),
		),
	),
	option : 'A?p?LiveProto????W',
);
```