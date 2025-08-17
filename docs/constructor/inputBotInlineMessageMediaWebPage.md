# inputBotInlineMessageMediaWebPage

**Description** : *Specifies options that will be used to generate the link preview for the message, or even a standalone link preview without an attached message*

**Layer** : 211

```tl
inputBotInlineMessageMediaWebPage#bddcc510 flags:# invert_media:flags.3?true force_large_media:flags.4?true force_small_media:flags.5?true optional:flags.6?true message:string entities:flags.1?Vector<MessageEntity> url:string reply_markup:flags.2?ReplyMarkup = InputBotInlineMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **invert_media** | [`flags.3?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| **force_large_media** | [`flags.4?true`](type/true) | If set, specifies that a large media preview should be used |
| **force_small_media** | [`flags.5?true`](type/true) | If set, specifies that a small media preview should be used |
| **optional** | [`flags.6?true`](type/true) | If not set, a WEBPAGE_NOT_FOUND RPC error will be emitted if a webpage preview cannot be generated for the specified url; otherwise, no error will be emitted (unless the provided message is also empty, in which case a MESSAGE_EMPTY will be emitted, instead) |
| <mark>message</mark> | [`string`](type/string) | The message, can be empty |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| <mark>url</mark> | [`string`](type/string) | The URL to use for the link preview |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Inline keyboard |

---

## Type

[InputBotInlineMessage](type/InputBotInlineMessage)

---

## Example

```php
$inputBotInlineMessage = $client->inputBotInlineMessageMediaWebPage(
	invert_media : true,
	force_large_media : true,
	force_small_media : true,
	optional : true,
	message : '1hQqCReYnaKBxkZV',
	entities : array(
		$client->messageEntityUnknown(
			offset : 24,
			length : 19,
		),
		$client->messageEntityMention(
			offset : 99,
			length : 23,
		),
		$client->messageEntityHashtag(
			offset : 98,
			length : 94,
		),
		$client->messageEntityBotCommand(
			offset : 29,
			length : 46,
		),
		$client->messageEntityUrl(
			offset : 3,
			length : 11,
		),
		$client->messageEntityEmail(
			offset : 95,
			length : 99,
		),
		$client->messageEntityBold(
			offset : 74,
			length : 6,
		),
		$client->messageEntityItalic(
			offset : 79,
			length : 42,
		),
		$client->messageEntityCode(
			offset : 99,
			length : 47,
		),
		$client->messageEntityPre(
			offset : 81,
			length : 75,
			language : 'l8w1pFyHsnLE2GAk',
		),
		$client->messageEntityTextUrl(
			offset : 83,
			length : 92,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 70,
			length : 20,
			user_id : 3954393454550095649,
		),
		$client->inputMessageEntityMentionName(
			offset : 80,
			length : 93,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 7,
			length : 99,
		),
		$client->messageEntityCashtag(
			offset : 57,
			length : 55,
		),
		$client->messageEntityUnderline(
			offset : 14,
			length : 97,
		),
		$client->messageEntityStrike(
			offset : 13,
			length : 41,
		),
		$client->messageEntityBankCard(
			offset : 100,
			length : 32,
		),
		$client->messageEntitySpoiler(
			offset : 56,
			length : 97,
		),
		$client->messageEntityCustomEmoji(
			offset : 73,
			length : 65,
			document_id : 594448868466605342,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 82,
			length : 65,
		),
	),
	url : 'https://docs.liveproto.dev',
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```