# botInlineMessageText

**Description** : *Send a simple text message*

**Layer** : 211

```tl
botInlineMessageText#8c7f65e2 flags:# no_webpage:flags.0?true invert_media:flags.3?true message:string entities:flags.1?Vector<MessageEntity> reply_markup:flags.2?ReplyMarkup = BotInlineMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **no_webpage** | [`flags.0?true`](type/true) | Disable webpage preview |
| **invert_media** | [`flags.3?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| <mark>message</mark> | [`string`](type/string) | The message |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Inline keyboard |

---

## Type

[BotInlineMessage](type/BotInlineMessage)

---

## Example

```php
$botInlineMessage = $client->botInlineMessageText(
	no_webpage : true,
	invert_media : true,
	message : 'v5rk0Bpw8lXIOo9e',
	entities : array(
		$client->messageEntityUnknown(
			offset : 55,
			length : 52,
		),
		$client->messageEntityMention(
			offset : 90,
			length : 36,
		),
		$client->messageEntityHashtag(
			offset : 9,
			length : 32,
		),
		$client->messageEntityBotCommand(
			offset : 70,
			length : 57,
		),
		$client->messageEntityUrl(
			offset : 91,
			length : 76,
		),
		$client->messageEntityEmail(
			offset : 84,
			length : 86,
		),
		$client->messageEntityBold(
			offset : 40,
			length : 18,
		),
		$client->messageEntityItalic(
			offset : 66,
			length : 33,
		),
		$client->messageEntityCode(
			offset : 52,
			length : 44,
		),
		$client->messageEntityPre(
			offset : 6,
			length : 19,
			language : 'ZvRwoPxnjQ02WmIJ',
		),
		$client->messageEntityTextUrl(
			offset : 9,
			length : 60,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 63,
			length : 30,
			user_id : -1138184684083818079,
		),
		$client->inputMessageEntityMentionName(
			offset : 96,
			length : 4,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 44,
			length : 51,
		),
		$client->messageEntityCashtag(
			offset : 18,
			length : 11,
		),
		$client->messageEntityUnderline(
			offset : 99,
			length : 23,
		),
		$client->messageEntityStrike(
			offset : 30,
			length : 13,
		),
		$client->messageEntityBankCard(
			offset : 31,
			length : 56,
		),
		$client->messageEntitySpoiler(
			offset : 82,
			length : 7,
		),
		$client->messageEntityCustomEmoji(
			offset : 15,
			length : 27,
			document_id : -8283065398413674737,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 21,
			length : 41,
		),
	),
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```