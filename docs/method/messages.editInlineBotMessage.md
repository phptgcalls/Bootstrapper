# messages.editInlineBotMessage

**Description** : *Edit an inline bot message*

**Layer** : 211

```tl
messages.editInlineBotMessage#83557dba flags:# no_webpage:flags.1?true invert_media:flags.16?true id:InputBotInlineMessageID message:flags.11?string media:flags.14?InputMedia reply_markup:flags.2?ReplyMarkup entities:flags.3?Vector<MessageEntity> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **no_webpage** | [`flags.1?true`](type/true) | Disable webpage preview |
| **invert_media** | [`flags.16?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| <mark>id</mark> | [`InputBotInlineMessageID`](type/InputBotInlineMessageID) | Sent inline message ID |
| **message** | [`flags.11?string`](type/string) | Message |
| **media** | [`flags.14?InputMedia`](type/InputMedia) | Media |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Reply markup for inline keyboards |
| **entities** | [`flags.3?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **BUTTON_DATA_INVALID** | `400` | The data of one or more of the buttons you provided is invalid |
| **ENTITY_BOUNDS_INVALID** | `400` | A specified entity offset or length is invalid, see here » for info on how to properly compute the entity offset/length |
| **MESSAGE_ID_INVALID** | `400` | The provided message id is invalid |
| **MESSAGE_NOT_MODIFIED** | `400` | The provided message data is identical to the previous message data, the message wasn't modified |

---

## Example

```php
$bool = $client->messages->editInlineBotMessage(
	no_webpage : true,
	invert_media : true,
	id : $client->inputBotInlineMessageID(
		dc_id : 61,
		id : 1690452234911284306,
		access_hash : -5162352911008254008,
	),
	message : 'KEnRAa6iIYOvNG9U',
	media : $client->inputMediaEmpty(),
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
	entities : array(
		$client->messageEntityUnknown(
			offset : 95,
			length : 87,
		),
		$client->messageEntityMention(
			offset : 15,
			length : 3,
		),
		$client->messageEntityHashtag(
			offset : 61,
			length : 74,
		),
		$client->messageEntityBotCommand(
			offset : 5,
			length : 4,
		),
		$client->messageEntityUrl(
			offset : 6,
			length : 48,
		),
		$client->messageEntityEmail(
			offset : 26,
			length : 35,
		),
		$client->messageEntityBold(
			offset : 98,
			length : 0,
		),
		$client->messageEntityItalic(
			offset : 80,
			length : 28,
		),
		$client->messageEntityCode(
			offset : 80,
			length : 48,
		),
		$client->messageEntityPre(
			offset : 27,
			length : 2,
			language : '6fRYhxjsXO9u1UQg',
		),
		$client->messageEntityTextUrl(
			offset : 76,
			length : 61,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 5,
			length : 81,
			user_id : 4273669573269448114,
		),
		$client->inputMessageEntityMentionName(
			offset : 44,
			length : 99,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 34,
			length : 34,
		),
		$client->messageEntityCashtag(
			offset : 44,
			length : 100,
		),
		$client->messageEntityUnderline(
			offset : 2,
			length : 17,
		),
		$client->messageEntityStrike(
			offset : 48,
			length : 10,
		),
		$client->messageEntityBankCard(
			offset : 11,
			length : 23,
		),
		$client->messageEntitySpoiler(
			offset : 60,
			length : 86,
		),
		$client->messageEntityCustomEmoji(
			offset : 86,
			length : 73,
			document_id : 6523291758903500536,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 16,
			length : 91,
		),
	),
);
```