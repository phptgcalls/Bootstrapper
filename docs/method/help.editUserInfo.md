# help.editUserInfo

**Description** : *Internal use*

**Layer** : 211

```tl
help.editUserInfo#66b91b70 user_id:InputUser message:string entities:Vector<MessageEntity> = help.UserInfo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>user_id</mark> | [`InputUser`](type/InputUser) | User |
| <mark>message</mark> | [`string`](type/string) | Message |
| <mark>entities</mark> | [`Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Result

[help.UserInfo](type/help.UserInfo)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **ENTITY_BOUNDS_INVALID** | `400` | A specified entity offset or length is invalid, see here » for info on how to properly compute the entity offset/length |
| **USER_INVALID** | `403` | Invalid user provided |

---

## Example

```php
$helpUserInfo = $client->help->editUserInfo(
	user_id : $client->inputUserEmpty(),
	message : 'pgTxD8CqeEaAfNFv',
	entities : array(
		$client->messageEntityUnknown(
			offset : 10,
			length : 88,
		),
		$client->messageEntityMention(
			offset : 8,
			length : 80,
		),
		$client->messageEntityHashtag(
			offset : 18,
			length : 18,
		),
		$client->messageEntityBotCommand(
			offset : 61,
			length : 87,
		),
		$client->messageEntityUrl(
			offset : 63,
			length : 50,
		),
		$client->messageEntityEmail(
			offset : 97,
			length : 31,
		),
		$client->messageEntityBold(
			offset : 49,
			length : 28,
		),
		$client->messageEntityItalic(
			offset : 0,
			length : 18,
		),
		$client->messageEntityCode(
			offset : 90,
			length : 96,
		),
		$client->messageEntityPre(
			offset : 1,
			length : 22,
			language : 'qHRJUdPAtBlN3r2w',
		),
		$client->messageEntityTextUrl(
			offset : 94,
			length : 3,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 23,
			length : 60,
			user_id : 1494633970001759927,
		),
		$client->inputMessageEntityMentionName(
			offset : 32,
			length : 40,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 41,
			length : 50,
		),
		$client->messageEntityCashtag(
			offset : 26,
			length : 60,
		),
		$client->messageEntityUnderline(
			offset : 27,
			length : 100,
		),
		$client->messageEntityStrike(
			offset : 83,
			length : 83,
		),
		$client->messageEntityBankCard(
			offset : 13,
			length : 11,
		),
		$client->messageEntitySpoiler(
			offset : 17,
			length : 76,
		),
		$client->messageEntityCustomEmoji(
			offset : 78,
			length : 68,
			document_id : 3614006587983883626,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 58,
			length : 33,
		),
	),
);
```