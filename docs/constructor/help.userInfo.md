# help.userInfo

**Description** : *Internal use*

**Layer** : 211

```tl
help.userInfo#1eb3758 message:string entities:Vector<MessageEntity> author:string date:int = help.UserInfo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>message</mark> | [`string`](type/string) | Info |
| <mark>entities</mark> | [`Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| <mark>author</mark> | [`string`](type/string) | Author |
| <mark>date</mark> | [`int`](type/int) | Date |

---

## Type

[help.UserInfo](type/help.UserInfo)

---

## Example

```php
$helpUserInfo = $client->help->userInfo(
	message : '4NGoQ295LgOHyRwY',
	entities : array(
		$client->messageEntityUnknown(
			offset : 19,
			length : 43,
		),
		$client->messageEntityMention(
			offset : 51,
			length : 7,
		),
		$client->messageEntityHashtag(
			offset : 48,
			length : 89,
		),
		$client->messageEntityBotCommand(
			offset : 0,
			length : 98,
		),
		$client->messageEntityUrl(
			offset : 20,
			length : 88,
		),
		$client->messageEntityEmail(
			offset : 62,
			length : 23,
		),
		$client->messageEntityBold(
			offset : 34,
			length : 16,
		),
		$client->messageEntityItalic(
			offset : 44,
			length : 98,
		),
		$client->messageEntityCode(
			offset : 37,
			length : 58,
		),
		$client->messageEntityPre(
			offset : 66,
			length : 85,
			language : 'ZhBTgDm5Rw4aELtd',
		),
		$client->messageEntityTextUrl(
			offset : 87,
			length : 33,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 55,
			length : 57,
			user_id : 1853808569430974139,
		),
		$client->inputMessageEntityMentionName(
			offset : 74,
			length : 40,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 80,
			length : 6,
		),
		$client->messageEntityCashtag(
			offset : 42,
			length : 52,
		),
		$client->messageEntityUnderline(
			offset : 82,
			length : 3,
		),
		$client->messageEntityStrike(
			offset : 74,
			length : 9,
		),
		$client->messageEntityBankCard(
			offset : 41,
			length : 26,
		),
		$client->messageEntitySpoiler(
			offset : 78,
			length : 19,
		),
		$client->messageEntityCustomEmoji(
			offset : 1,
			length : 92,
			document_id : -4393969921118190635,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 3,
			length : 93,
		),
	),
	author : 'wly7W5E1jPFeibgx',
	date : 26,
);
```