# botInlineMessageMediaWebPage

**Description** : *Specifies options that must be used to generate the link preview for the message, or even a standalone link preview without an attached message*

**Layer** : 211

```tl
botInlineMessageMediaWebPage#809ad9a6 flags:# invert_media:flags.3?true force_large_media:flags.4?true force_small_media:flags.5?true manual:flags.7?true safe:flags.8?true message:string entities:flags.1?Vector<MessageEntity> url:string reply_markup:flags.2?ReplyMarkup = BotInlineMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **invert_media** | [`flags.3?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| **force_large_media** | [`flags.4?true`](type/true) | If set, specifies that a large media preview should be used |
| **force_small_media** | [`flags.5?true`](type/true) | If set, specifies that a small media preview should be used |
| **manual** | [`flags.7?true`](type/true) | If set, indicates that the URL used for the webpage preview was specified manually using inputMediaWebPage, and may not be related to any of the URLs specified in the message |
| **safe** | [`flags.8?true`](type/true) | If set, the link can be opened directly without user confirmation |
| <mark>message</mark> | [`string`](type/string) | The message, can be empty |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| <mark>url</mark> | [`string`](type/string) | The URL to use for the link preview |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Reply markup for sending bot buttons |

---

## Type

[BotInlineMessage](type/BotInlineMessage)

---

## Example

```php
$botInlineMessage = $client->botInlineMessageMediaWebPage(
	invert_media : true,
	force_large_media : true,
	force_small_media : true,
	manual : true,
	safe : true,
	message : 'C3IsKDYVXuNO7an6',
	entities : array(
		$client->messageEntityUnknown(
			offset : 72,
			length : 91,
		),
		$client->messageEntityMention(
			offset : 31,
			length : 20,
		),
		$client->messageEntityHashtag(
			offset : 84,
			length : 73,
		),
		$client->messageEntityBotCommand(
			offset : 0,
			length : 29,
		),
		$client->messageEntityUrl(
			offset : 6,
			length : 70,
		),
		$client->messageEntityEmail(
			offset : 32,
			length : 75,
		),
		$client->messageEntityBold(
			offset : 28,
			length : 84,
		),
		$client->messageEntityItalic(
			offset : 68,
			length : 22,
		),
		$client->messageEntityCode(
			offset : 100,
			length : 25,
		),
		$client->messageEntityPre(
			offset : 27,
			length : 4,
			language : 'raNsXYMWJnROT4QD',
		),
		$client->messageEntityTextUrl(
			offset : 61,
			length : 83,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 23,
			length : 50,
			user_id : 5704116416666723235,
		),
		$client->inputMessageEntityMentionName(
			offset : 41,
			length : 39,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 41,
			length : 28,
		),
		$client->messageEntityCashtag(
			offset : 29,
			length : 49,
		),
		$client->messageEntityUnderline(
			offset : 6,
			length : 12,
		),
		$client->messageEntityStrike(
			offset : 24,
			length : 48,
		),
		$client->messageEntityBankCard(
			offset : 16,
			length : 100,
		),
		$client->messageEntitySpoiler(
			offset : 50,
			length : 97,
		),
		$client->messageEntityCustomEmoji(
			offset : 57,
			length : 19,
			document_id : 7782566177726111355,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 35,
			length : 49,
		),
	),
	url : 'https://docs.liveproto.dev',
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```