# inputBotInlineResultPhoto

**Description** : *Photo*

**Layer** : 211

```tl
inputBotInlineResultPhoto#a8d864a7 id:string type:string photo:InputPhoto send_message:InputBotInlineMessage = InputBotInlineResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`string`](type/string) | Result ID |
| <mark>type</mark> | [`string`](type/string) | Result type (see bot API docs) |
| <mark>photo</mark> | [`InputPhoto`](type/InputPhoto) | Photo to send |
| <mark>send_message</mark> | [`InputBotInlineMessage`](type/InputBotInlineMessage) | Message to send when the result is selected |

---

## Type

[InputBotInlineResult](type/InputBotInlineResult)

---

## Example

```php
$inputBotInlineResult = $client->inputBotInlineResultPhoto(
	id : 'GXtvALgkNeUSflb0',
	type : 'wtySmhE8MoH9qxWk',
	photo : $client->inputPhotoEmpty(),
	send_message : $client->inputBotInlineMessageMediaAuto(
		invert_media : true,
		message : 'BciuxSG5k98TpNMQ',
		entities : array(
			$client->messageEntityUnknown(
				offset : 82,
				length : 49,
			),
			$client->messageEntityMention(
				offset : 9,
				length : 18,
			),
			$client->messageEntityHashtag(
				offset : 25,
				length : 37,
			),
			$client->messageEntityBotCommand(
				offset : 38,
				length : 86,
			),
			$client->messageEntityUrl(
				offset : 81,
				length : 59,
			),
			$client->messageEntityEmail(
				offset : 56,
				length : 11,
			),
			$client->messageEntityBold(
				offset : 99,
				length : 52,
			),
			$client->messageEntityItalic(
				offset : 69,
				length : 87,
			),
			$client->messageEntityCode(
				offset : 99,
				length : 86,
			),
			$client->messageEntityPre(
				offset : 95,
				length : 97,
				language : 'vh9bqX61xsTga0cJ',
			),
			$client->messageEntityTextUrl(
				offset : 78,
				length : 82,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 50,
				length : 23,
				user_id : -6529590889281976336,
			),
			$client->inputMessageEntityMentionName(
				offset : 63,
				length : 36,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 65,
				length : 53,
			),
			$client->messageEntityCashtag(
				offset : 48,
				length : 13,
			),
			$client->messageEntityUnderline(
				offset : 66,
				length : 95,
			),
			$client->messageEntityStrike(
				offset : 99,
				length : 72,
			),
			$client->messageEntityBankCard(
				offset : 17,
				length : 86,
			),
			$client->messageEntitySpoiler(
				offset : 56,
				length : 36,
			),
			$client->messageEntityCustomEmoji(
				offset : 92,
				length : 95,
				document_id : 3980514018584667699,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 99,
				length : 27,
			),
		),
		reply_markup : $client->replyKeyboardHide(
			selective : true,
		),
	),
);
```