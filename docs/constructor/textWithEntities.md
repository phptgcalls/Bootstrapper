# textWithEntities

**Description** : *Styled text with message entities*

**Layer** : 211

```tl
textWithEntities#751f3146 text:string entities:Vector<MessageEntity> = TextWithEntities;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>text</mark> | [`string`](type/string) | Text |
| <mark>entities</mark> | [`Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Type

[TextWithEntities](type/TextWithEntities)

---

## Example

```php
$textWithEntities = $client->textWithEntities(
	text : 's06ew3RZfSkJOCMV',
	entities : array(
		$client->messageEntityUnknown(
			offset : 90,
			length : 26,
		),
		$client->messageEntityMention(
			offset : 98,
			length : 93,
		),
		$client->messageEntityHashtag(
			offset : 70,
			length : 72,
		),
		$client->messageEntityBotCommand(
			offset : 48,
			length : 86,
		),
		$client->messageEntityUrl(
			offset : 7,
			length : 99,
		),
		$client->messageEntityEmail(
			offset : 55,
			length : 65,
		),
		$client->messageEntityBold(
			offset : 16,
			length : 74,
		),
		$client->messageEntityItalic(
			offset : 64,
			length : 93,
		),
		$client->messageEntityCode(
			offset : 52,
			length : 28,
		),
		$client->messageEntityPre(
			offset : 58,
			length : 64,
			language : '0vcW3hj1CxVD9yEm',
		),
		$client->messageEntityTextUrl(
			offset : 31,
			length : 95,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 15,
			length : 40,
			user_id : 6635481361095987362,
		),
		$client->inputMessageEntityMentionName(
			offset : 87,
			length : 54,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 93,
			length : 98,
		),
		$client->messageEntityCashtag(
			offset : 33,
			length : 84,
		),
		$client->messageEntityUnderline(
			offset : 13,
			length : 69,
		),
		$client->messageEntityStrike(
			offset : 47,
			length : 21,
		),
		$client->messageEntityBankCard(
			offset : 22,
			length : 99,
		),
		$client->messageEntitySpoiler(
			offset : 58,
			length : 31,
		),
		$client->messageEntityCustomEmoji(
			offset : 10,
			length : 47,
			document_id : -8026171063172968579,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 13,
			length : 2,
		),
	),
);
```