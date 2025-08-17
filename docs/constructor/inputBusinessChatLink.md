# inputBusinessChatLink

**Description** : *Contains info about a business chat deep link » to be created by the current account*

**Layer** : 211

```tl
inputBusinessChatLink#11679fa7 flags:# message:string entities:flags.0?Vector<MessageEntity> title:flags.1?string = InputBusinessChatLink;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>message</mark> | [`string`](type/string) | Message to pre-fill in the message input field |
| **entities** | [`flags.0?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **title** | [`flags.1?string`](type/string) | Human-readable name of the link, to simplify management in the UI (only visible to the creator of the link) |

---

## Type

[InputBusinessChatLink](type/InputBusinessChatLink)

---

## Example

```php
$inputBusinessChatLink = $client->inputBusinessChatLink(
	message : 'jdlWCARcg1rzaFVu',
	entities : array(
		$client->messageEntityUnknown(
			offset : 31,
			length : 90,
		),
		$client->messageEntityMention(
			offset : 17,
			length : 51,
		),
		$client->messageEntityHashtag(
			offset : 95,
			length : 48,
		),
		$client->messageEntityBotCommand(
			offset : 5,
			length : 46,
		),
		$client->messageEntityUrl(
			offset : 27,
			length : 94,
		),
		$client->messageEntityEmail(
			offset : 5,
			length : 92,
		),
		$client->messageEntityBold(
			offset : 99,
			length : 32,
		),
		$client->messageEntityItalic(
			offset : 96,
			length : 7,
		),
		$client->messageEntityCode(
			offset : 82,
			length : 21,
		),
		$client->messageEntityPre(
			offset : 98,
			length : 41,
			language : 'vC5MHVyuS7KkdULb',
		),
		$client->messageEntityTextUrl(
			offset : 47,
			length : 26,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 86,
			length : 19,
			user_id : -6255664682297907619,
		),
		$client->inputMessageEntityMentionName(
			offset : 84,
			length : 68,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 36,
			length : 74,
		),
		$client->messageEntityCashtag(
			offset : 87,
			length : 88,
		),
		$client->messageEntityUnderline(
			offset : 26,
			length : 61,
		),
		$client->messageEntityStrike(
			offset : 27,
			length : 21,
		),
		$client->messageEntityBankCard(
			offset : 89,
			length : 100,
		),
		$client->messageEntitySpoiler(
			offset : 57,
			length : 41,
		),
		$client->messageEntityCustomEmoji(
			offset : 97,
			length : 42,
			document_id : 2544846939349709738,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 39,
			length : 96,
		),
	),
	title : 'RrSDVuQYyXakqjM4',
);
```