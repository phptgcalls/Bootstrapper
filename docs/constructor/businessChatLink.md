# businessChatLink

**Description** : *Contains info about a business chat deep link » created by the current account*

**Layer** : 211

```tl
businessChatLink#b4ae666f flags:# link:string message:string entities:flags.0?Vector<MessageEntity> title:flags.1?string views:int = BusinessChatLink;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>link</mark> | [`string`](type/string) | Business chat deep link |
| <mark>message</mark> | [`string`](type/string) | Message to pre-fill in the message input field |
| **entities** | [`flags.0?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **title** | [`flags.1?string`](type/string) | Human-readable name of the link, to simplify management in the UI (only visible to the creator of the link) |
| <mark>views</mark> | [`int`](type/int) | Number of times the link was resolved (clicked/scanned/etc...) |

---

## Type

[BusinessChatLink](type/BusinessChatLink)

---

## Example

```php
$businessChatLink = $client->businessChatLink(
	link : 'kzfhUboBJIOiT2HV',
	message : 'WrHIqvdAZCG3pfVL',
	entities : array(
		$client->messageEntityUnknown(
			offset : 50,
			length : 33,
		),
		$client->messageEntityMention(
			offset : 44,
			length : 42,
		),
		$client->messageEntityHashtag(
			offset : 99,
			length : 85,
		),
		$client->messageEntityBotCommand(
			offset : 98,
			length : 49,
		),
		$client->messageEntityUrl(
			offset : 71,
			length : 57,
		),
		$client->messageEntityEmail(
			offset : 7,
			length : 86,
		),
		$client->messageEntityBold(
			offset : 82,
			length : 42,
		),
		$client->messageEntityItalic(
			offset : 98,
			length : 42,
		),
		$client->messageEntityCode(
			offset : 20,
			length : 35,
		),
		$client->messageEntityPre(
			offset : 61,
			length : 9,
			language : 'RDurvNLqd3fKEy19',
		),
		$client->messageEntityTextUrl(
			offset : 59,
			length : 53,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 63,
			length : 55,
			user_id : -1491559027378511654,
		),
		$client->inputMessageEntityMentionName(
			offset : 33,
			length : 63,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 11,
			length : 12,
		),
		$client->messageEntityCashtag(
			offset : 1,
			length : 52,
		),
		$client->messageEntityUnderline(
			offset : 17,
			length : 44,
		),
		$client->messageEntityStrike(
			offset : 16,
			length : 0,
		),
		$client->messageEntityBankCard(
			offset : 37,
			length : 68,
		),
		$client->messageEntitySpoiler(
			offset : 88,
			length : 60,
		),
		$client->messageEntityCustomEmoji(
			offset : 4,
			length : 10,
			document_id : -4754674682617307715,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 58,
			length : 87,
		),
	),
	title : 'Cu5mbRpQqY1PiVeo',
	views : 75,
);
```