# botInlineMessageMediaAuto

**Description** : *Send whatever media is attached to the botInlineMediaResult*

**Layer** : 211

```tl
botInlineMessageMediaAuto#764cf810 flags:# invert_media:flags.3?true message:string entities:flags.1?Vector<MessageEntity> reply_markup:flags.2?ReplyMarkup = BotInlineMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **invert_media** | [`flags.3?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| <mark>message</mark> | [`string`](type/string) | Caption |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Inline keyboard |

---

## Type

[BotInlineMessage](type/BotInlineMessage)

---

## Example

```php
$botInlineMessage = $client->botInlineMessageMediaAuto(
	invert_media : true,
	message : 'QBI3CnsY4z5c7ALj',
	entities : array(
		$client->messageEntityUnknown(
			offset : 71,
			length : 57,
		),
		$client->messageEntityMention(
			offset : 60,
			length : 39,
		),
		$client->messageEntityHashtag(
			offset : 75,
			length : 49,
		),
		$client->messageEntityBotCommand(
			offset : 0,
			length : 0,
		),
		$client->messageEntityUrl(
			offset : 78,
			length : 92,
		),
		$client->messageEntityEmail(
			offset : 13,
			length : 67,
		),
		$client->messageEntityBold(
			offset : 99,
			length : 41,
		),
		$client->messageEntityItalic(
			offset : 20,
			length : 61,
		),
		$client->messageEntityCode(
			offset : 59,
			length : 86,
		),
		$client->messageEntityPre(
			offset : 62,
			length : 75,
			language : 'YQ2pFcKv4HN50Sim',
		),
		$client->messageEntityTextUrl(
			offset : 22,
			length : 12,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 53,
			length : 80,
			user_id : -5633444093261455338,
		),
		$client->inputMessageEntityMentionName(
			offset : 16,
			length : 28,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 27,
			length : 35,
		),
		$client->messageEntityCashtag(
			offset : 61,
			length : 70,
		),
		$client->messageEntityUnderline(
			offset : 9,
			length : 19,
		),
		$client->messageEntityStrike(
			offset : 38,
			length : 47,
		),
		$client->messageEntityBankCard(
			offset : 22,
			length : 76,
		),
		$client->messageEntitySpoiler(
			offset : 6,
			length : 15,
		),
		$client->messageEntityCustomEmoji(
			offset : 49,
			length : 73,
			document_id : -3730490343020365477,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 12,
			length : 27,
		),
	),
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```