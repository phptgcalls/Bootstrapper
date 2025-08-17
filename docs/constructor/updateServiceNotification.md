# updateServiceNotification

**Description** : *A service message for the user*

**Layer** : 211

```tl
updateServiceNotification#ebe46819 flags:# popup:flags.0?true invert_media:flags.2?true inbox_date:flags.1?int type:string message:string media:MessageMedia entities:Vector<MessageEntity> = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **popup** | [`flags.0?true`](type/true) | If set, the message must be displayed in a popup |
| **invert_media** | [`flags.2?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| **inbox_date** | [`flags.1?int`](type/int) | When was the notification receivedThe message must also be stored locally as part of the message history with the user id 777000 (Telegram Notifications) |
| <mark>type</mark> | [`string`](type/string) | String, identical in format and contents to the type field in API errors. Describes type of service message. It is acceptable to ignore repeated messages of the same type within a short period of time (15 minutes) |
| <mark>message</mark> | [`string`](type/string) | Message text |
| <mark>media</mark> | [`MessageMedia`](type/MessageMedia) | Media content (optional) |
| <mark>entities</mark> | [`Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateServiceNotification(
	popup : true,
	invert_media : true,
	inbox_date : 37,
	type : 'Tgj1kBFxqoyHJV0K',
	message : '7oKbxvB0MmErkVWu',
	media : $client->messageMediaEmpty(),
	entities : array(
		$client->messageEntityUnknown(
			offset : 42,
			length : 50,
		),
		$client->messageEntityMention(
			offset : 37,
			length : 20,
		),
		$client->messageEntityHashtag(
			offset : 13,
			length : 48,
		),
		$client->messageEntityBotCommand(
			offset : 6,
			length : 40,
		),
		$client->messageEntityUrl(
			offset : 100,
			length : 68,
		),
		$client->messageEntityEmail(
			offset : 5,
			length : 63,
		),
		$client->messageEntityBold(
			offset : 6,
			length : 69,
		),
		$client->messageEntityItalic(
			offset : 15,
			length : 57,
		),
		$client->messageEntityCode(
			offset : 9,
			length : 46,
		),
		$client->messageEntityPre(
			offset : 64,
			length : 31,
			language : 'ETNOvHsSxy6Pi7bA',
		),
		$client->messageEntityTextUrl(
			offset : 4,
			length : 78,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 54,
			length : 47,
			user_id : -7417495754971225762,
		),
		$client->inputMessageEntityMentionName(
			offset : 85,
			length : 25,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 14,
			length : 14,
		),
		$client->messageEntityCashtag(
			offset : 37,
			length : 77,
		),
		$client->messageEntityUnderline(
			offset : 49,
			length : 23,
		),
		$client->messageEntityStrike(
			offset : 95,
			length : 82,
		),
		$client->messageEntityBankCard(
			offset : 55,
			length : 65,
		),
		$client->messageEntitySpoiler(
			offset : 79,
			length : 6,
		),
		$client->messageEntityCustomEmoji(
			offset : 25,
			length : 96,
			document_id : -345788071062806228,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 90,
			length : 18,
		),
	),
);
```