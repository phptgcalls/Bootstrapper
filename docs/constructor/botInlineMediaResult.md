# botInlineMediaResult

**Description** : *Media result*

**Layer** : 211

```tl
botInlineMediaResult#17db940b flags:# id:string type:string photo:flags.0?Photo document:flags.1?Document title:flags.2?string description:flags.3?string send_message:BotInlineMessage = BotInlineResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>id</mark> | [`string`](type/string) | Result ID |
| <mark>type</mark> | [`string`](type/string) | Result type (see bot API docs) |
| **photo** | [`flags.0?Photo`](type/Photo) | If type is photo, the photo to send |
| **document** | [`flags.1?Document`](type/Document) | If type is document, the document to send |
| **title** | [`flags.2?string`](type/string) | Result title |
| **description** | [`flags.3?string`](type/string) | Description |
| <mark>send_message</mark> | [`BotInlineMessage`](type/BotInlineMessage) | Depending on the type and on the constructor, contains the caption of the media or the content of the message to be sent instead of the media |

---

## Type

[BotInlineResult](type/BotInlineResult)

---

## Example

```php
$botInlineResult = $client->botInlineMediaResult(
	id : 'l5A9Qa3hbBTFuLGZ',
	type : 'Fmy5Vnq2GHPh4ANQ',
	photo : $client->photoEmpty(
		id : -619875691066323025,
	),
	document : $client->documentEmpty(
		id : -6194564310200045412,
	),
	title : 'wJAjRsLTYCWqEOx7',
	description : 'uMC3a8Rf4G1xAy2J',
	send_message : $client->botInlineMessageMediaAuto(
		invert_media : true,
		message : 'EFbv6eHczkPq78hr',
		entities : array(
			$client->messageEntityUnknown(
				offset : 100,
				length : 53,
			),
			$client->messageEntityMention(
				offset : 49,
				length : 30,
			),
			$client->messageEntityHashtag(
				offset : 46,
				length : 32,
			),
			$client->messageEntityBotCommand(
				offset : 66,
				length : 7,
			),
			$client->messageEntityUrl(
				offset : 5,
				length : 48,
			),
			$client->messageEntityEmail(
				offset : 80,
				length : 72,
			),
			$client->messageEntityBold(
				offset : 20,
				length : 75,
			),
			$client->messageEntityItalic(
				offset : 79,
				length : 44,
			),
			$client->messageEntityCode(
				offset : 87,
				length : 60,
			),
			$client->messageEntityPre(
				offset : 52,
				length : 97,
				language : 'gaCxJF48MemXkY2p',
			),
			$client->messageEntityTextUrl(
				offset : 20,
				length : 21,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 65,
				length : 76,
				user_id : 6490671909171294394,
			),
			$client->inputMessageEntityMentionName(
				offset : 31,
				length : 32,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 34,
				length : 19,
			),
			$client->messageEntityCashtag(
				offset : 50,
				length : 8,
			),
			$client->messageEntityUnderline(
				offset : 75,
				length : 81,
			),
			$client->messageEntityStrike(
				offset : 7,
				length : 51,
			),
			$client->messageEntityBankCard(
				offset : 88,
				length : 52,
			),
			$client->messageEntitySpoiler(
				offset : 75,
				length : 67,
			),
			$client->messageEntityCustomEmoji(
				offset : 44,
				length : 34,
				document_id : 9196763074967894460,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 1,
				length : 26,
			),
		),
		reply_markup : $client->replyKeyboardHide(
			selective : true,
		),
	),
);
```