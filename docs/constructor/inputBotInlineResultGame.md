# inputBotInlineResultGame

**Description** : *Game*

**Layer** : 211

```tl
inputBotInlineResultGame#4fa417f2 id:string short_name:string send_message:InputBotInlineMessage = InputBotInlineResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`string`](type/string) | Result ID |
| <mark>short_name</mark> | [`string`](type/string) | Game short name |
| <mark>send_message</mark> | [`InputBotInlineMessage`](type/InputBotInlineMessage) | Message to send when the result is selected |

---

## Type

[InputBotInlineResult](type/InputBotInlineResult)

---

## Example

```php
$inputBotInlineResult = $client->inputBotInlineResultGame(
	id : '0mEOZF3ebwV4CBtQ',
	short_name : '3s01kTwChHJdot6Y',
	send_message : $client->inputBotInlineMessageMediaAuto(
		invert_media : true,
		message : 'RLmqg8D7fHpQPVKG',
		entities : array(
			$client->messageEntityUnknown(
				offset : 14,
				length : 71,
			),
			$client->messageEntityMention(
				offset : 32,
				length : 58,
			),
			$client->messageEntityHashtag(
				offset : 26,
				length : 71,
			),
			$client->messageEntityBotCommand(
				offset : 5,
				length : 6,
			),
			$client->messageEntityUrl(
				offset : 70,
				length : 24,
			),
			$client->messageEntityEmail(
				offset : 3,
				length : 73,
			),
			$client->messageEntityBold(
				offset : 8,
				length : 60,
			),
			$client->messageEntityItalic(
				offset : 63,
				length : 36,
			),
			$client->messageEntityCode(
				offset : 73,
				length : 58,
			),
			$client->messageEntityPre(
				offset : 35,
				length : 37,
				language : 'rWpIYcNFGJvbj8uM',
			),
			$client->messageEntityTextUrl(
				offset : 1,
				length : 22,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 24,
				length : 4,
				user_id : -7866537513414845382,
			),
			$client->inputMessageEntityMentionName(
				offset : 2,
				length : 23,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 71,
				length : 99,
			),
			$client->messageEntityCashtag(
				offset : 46,
				length : 39,
			),
			$client->messageEntityUnderline(
				offset : 98,
				length : 10,
			),
			$client->messageEntityStrike(
				offset : 5,
				length : 97,
			),
			$client->messageEntityBankCard(
				offset : 15,
				length : 78,
			),
			$client->messageEntitySpoiler(
				offset : 16,
				length : 70,
			),
			$client->messageEntityCustomEmoji(
				offset : 63,
				length : 46,
				document_id : -6384689204022508433,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 68,
				length : 7,
			),
		),
		reply_markup : $client->replyKeyboardHide(
			selective : true,
		),
	),
);
```