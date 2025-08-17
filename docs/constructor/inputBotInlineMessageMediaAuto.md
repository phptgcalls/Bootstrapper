# inputBotInlineMessageMediaAuto

**Description** : *A media*

**Layer** : 211

```tl
inputBotInlineMessageMediaAuto#3380c786 flags:# invert_media:flags.3?true message:string entities:flags.1?Vector<MessageEntity> reply_markup:flags.2?ReplyMarkup = InputBotInlineMessage;
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

[InputBotInlineMessage](type/InputBotInlineMessage)

---

## Example

```php
$inputBotInlineMessage = $client->inputBotInlineMessageMediaAuto(
	invert_media : true,
	message : 'zjcgR2V7UQ5S4FxX',
	entities : array(
		$client->messageEntityUnknown(
			offset : 63,
			length : 75,
		),
		$client->messageEntityMention(
			offset : 30,
			length : 1,
		),
		$client->messageEntityHashtag(
			offset : 0,
			length : 50,
		),
		$client->messageEntityBotCommand(
			offset : 4,
			length : 10,
		),
		$client->messageEntityUrl(
			offset : 29,
			length : 41,
		),
		$client->messageEntityEmail(
			offset : 7,
			length : 18,
		),
		$client->messageEntityBold(
			offset : 56,
			length : 55,
		),
		$client->messageEntityItalic(
			offset : 19,
			length : 13,
		),
		$client->messageEntityCode(
			offset : 17,
			length : 26,
		),
		$client->messageEntityPre(
			offset : 78,
			length : 10,
			language : '0IkYlwXK8zP4qQjJ',
		),
		$client->messageEntityTextUrl(
			offset : 64,
			length : 92,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 25,
			length : 79,
			user_id : 4264366796081111277,
		),
		$client->inputMessageEntityMentionName(
			offset : 28,
			length : 4,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 96,
			length : 17,
		),
		$client->messageEntityCashtag(
			offset : 6,
			length : 26,
		),
		$client->messageEntityUnderline(
			offset : 60,
			length : 4,
		),
		$client->messageEntityStrike(
			offset : 13,
			length : 6,
		),
		$client->messageEntityBankCard(
			offset : 100,
			length : 18,
		),
		$client->messageEntitySpoiler(
			offset : 48,
			length : 50,
		),
		$client->messageEntityCustomEmoji(
			offset : 43,
			length : 3,
			document_id : 111071842454115896,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 36,
			length : 49,
		),
	),
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```