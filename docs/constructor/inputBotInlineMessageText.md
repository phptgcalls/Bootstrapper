# inputBotInlineMessageText

**Description** : *Simple text message*

**Layer** : 211

```tl
inputBotInlineMessageText#3dcd7a87 flags:# no_webpage:flags.0?true invert_media:flags.3?true message:string entities:flags.1?Vector<MessageEntity> reply_markup:flags.2?ReplyMarkup = InputBotInlineMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **no_webpage** | [`flags.0?true`](type/true) | Disable webpage preview |
| **invert_media** | [`flags.3?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| <mark>message</mark> | [`string`](type/string) | Message |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Inline keyboard |

---

## Type

[InputBotInlineMessage](type/InputBotInlineMessage)

---

## Example

```php
$inputBotInlineMessage = $client->inputBotInlineMessageText(
	no_webpage : true,
	invert_media : true,
	message : 'dJ8S5X7qiTyj93D2',
	entities : array(
		$client->messageEntityUnknown(
			offset : 93,
			length : 51,
		),
		$client->messageEntityMention(
			offset : 53,
			length : 14,
		),
		$client->messageEntityHashtag(
			offset : 11,
			length : 93,
		),
		$client->messageEntityBotCommand(
			offset : 53,
			length : 44,
		),
		$client->messageEntityUrl(
			offset : 27,
			length : 74,
		),
		$client->messageEntityEmail(
			offset : 32,
			length : 43,
		),
		$client->messageEntityBold(
			offset : 73,
			length : 69,
		),
		$client->messageEntityItalic(
			offset : 69,
			length : 69,
		),
		$client->messageEntityCode(
			offset : 41,
			length : 94,
		),
		$client->messageEntityPre(
			offset : 72,
			length : 33,
			language : '0RNJwapQ9vD8EAGh',
		),
		$client->messageEntityTextUrl(
			offset : 34,
			length : 34,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 1,
			length : 13,
			user_id : -6115533931740739167,
		),
		$client->inputMessageEntityMentionName(
			offset : 31,
			length : 78,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 8,
			length : 89,
		),
		$client->messageEntityCashtag(
			offset : 25,
			length : 75,
		),
		$client->messageEntityUnderline(
			offset : 98,
			length : 16,
		),
		$client->messageEntityStrike(
			offset : 95,
			length : 24,
		),
		$client->messageEntityBankCard(
			offset : 62,
			length : 6,
		),
		$client->messageEntitySpoiler(
			offset : 87,
			length : 46,
		),
		$client->messageEntityCustomEmoji(
			offset : 24,
			length : 79,
			document_id : 3984202550712004824,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 96,
			length : 16,
		),
	),
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```