# inputBotInlineResultDocument

**Description** : *Document (media of any type except for photos)*

**Layer** : 211

```tl
inputBotInlineResultDocument#fff8fdc4 flags:# id:string type:string title:flags.1?string description:flags.2?string document:InputDocument send_message:InputBotInlineMessage = InputBotInlineResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>id</mark> | [`string`](type/string) | Result ID |
| <mark>type</mark> | [`string`](type/string) | Result type (see bot API docs) |
| **title** | [`flags.1?string`](type/string) | Result title |
| **description** | [`flags.2?string`](type/string) | Result description |
| <mark>document</mark> | [`InputDocument`](type/InputDocument) | Document to send |
| <mark>send_message</mark> | [`InputBotInlineMessage`](type/InputBotInlineMessage) | Message to send when the result is selected |

---

## Type

[InputBotInlineResult](type/InputBotInlineResult)

---

## Example

```php
$inputBotInlineResult = $client->inputBotInlineResultDocument(
	id : 'rn6DXi9ZKUzP3Rxa',
	type : '7tFVNzbXwx1sOjgr',
	title : 'MQA8kjOt96GhfVbp',
	description : 'I6zyrM84sWHYjLmV',
	document : $client->inputDocumentEmpty(),
	send_message : $client->inputBotInlineMessageMediaAuto(
		invert_media : true,
		message : '4hgzCp9DkxGtqa3Y',
		entities : array(
			$client->messageEntityUnknown(
				offset : 14,
				length : 62,
			),
			$client->messageEntityMention(
				offset : 4,
				length : 28,
			),
			$client->messageEntityHashtag(
				offset : 15,
				length : 22,
			),
			$client->messageEntityBotCommand(
				offset : 84,
				length : 51,
			),
			$client->messageEntityUrl(
				offset : 10,
				length : 27,
			),
			$client->messageEntityEmail(
				offset : 62,
				length : 87,
			),
			$client->messageEntityBold(
				offset : 63,
				length : 34,
			),
			$client->messageEntityItalic(
				offset : 30,
				length : 93,
			),
			$client->messageEntityCode(
				offset : 9,
				length : 36,
			),
			$client->messageEntityPre(
				offset : 91,
				length : 79,
				language : 'XQlBtmnzYSs9c6kM',
			),
			$client->messageEntityTextUrl(
				offset : 18,
				length : 72,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 63,
				length : 38,
				user_id : 2039382914200765356,
			),
			$client->inputMessageEntityMentionName(
				offset : 86,
				length : 40,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 84,
				length : 78,
			),
			$client->messageEntityCashtag(
				offset : 41,
				length : 17,
			),
			$client->messageEntityUnderline(
				offset : 30,
				length : 23,
			),
			$client->messageEntityStrike(
				offset : 12,
				length : 63,
			),
			$client->messageEntityBankCard(
				offset : 36,
				length : 5,
			),
			$client->messageEntitySpoiler(
				offset : 15,
				length : 51,
			),
			$client->messageEntityCustomEmoji(
				offset : 1,
				length : 31,
				document_id : -5703974405195653829,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 33,
				length : 89,
			),
		),
		reply_markup : $client->replyKeyboardHide(
			selective : true,
		),
	),
);
```