# help.termsOfService

**Description** : *Info about the latest telegram Terms Of Service*

**Layer** : 211

```tl
help.termsOfService#780a0310 flags:# popup:flags.0?true id:DataJSON text:string entities:Vector<MessageEntity> min_age_confirm:flags.1?int = help.TermsOfService;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **popup** | [`flags.0?true`](type/true) | Whether a prompt must be showed to the user, in order to accept the new terms |
| <mark>id</mark> | [`DataJSON`](type/DataJSON) | ID of the new terms |
| <mark>text</mark> | [`string`](type/string) | Text of the new terms |
| <mark>entities</mark> | [`Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **min_age_confirm** | [`flags.1?int`](type/int) | Minimum age required to sign up to telegram, the user must confirm that they is older than the minimum age |

---

## Type

[help.TermsOfService](type/help.TermsOfService)

---

## Example

```php
$helpTermsOfService = $client->help->termsOfService(
	popup : true,
	id : $client->dataJSON(
		data : 'u5m6LP7eagcKn4Qf',
	),
	text : 'k5saB1ZTUo0qpKn2',
	entities : array(
		$client->messageEntityUnknown(
			offset : 6,
			length : 39,
		),
		$client->messageEntityMention(
			offset : 28,
			length : 19,
		),
		$client->messageEntityHashtag(
			offset : 39,
			length : 90,
		),
		$client->messageEntityBotCommand(
			offset : 76,
			length : 48,
		),
		$client->messageEntityUrl(
			offset : 63,
			length : 46,
		),
		$client->messageEntityEmail(
			offset : 9,
			length : 32,
		),
		$client->messageEntityBold(
			offset : 65,
			length : 97,
		),
		$client->messageEntityItalic(
			offset : 53,
			length : 86,
		),
		$client->messageEntityCode(
			offset : 8,
			length : 62,
		),
		$client->messageEntityPre(
			offset : 66,
			length : 74,
			language : '2HTwDnM4jm7vOXeC',
		),
		$client->messageEntityTextUrl(
			offset : 15,
			length : 0,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 35,
			length : 86,
			user_id : -2834243862188755001,
		),
		$client->inputMessageEntityMentionName(
			offset : 45,
			length : 12,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 95,
			length : 81,
		),
		$client->messageEntityCashtag(
			offset : 23,
			length : 3,
		),
		$client->messageEntityUnderline(
			offset : 25,
			length : 91,
		),
		$client->messageEntityStrike(
			offset : 23,
			length : 2,
		),
		$client->messageEntityBankCard(
			offset : 66,
			length : 49,
		),
		$client->messageEntitySpoiler(
			offset : 84,
			length : 65,
		),
		$client->messageEntityCustomEmoji(
			offset : 63,
			length : 3,
			document_id : -1732080007315043025,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 84,
			length : 44,
		),
	),
	min_age_confirm : 22,
);
```