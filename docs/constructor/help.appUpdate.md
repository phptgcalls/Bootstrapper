# help.appUpdate

**Description** : *An update is available for the application*

**Layer** : 211

```tl
help.appUpdate#ccbbce30 flags:# can_not_skip:flags.0?true id:int version:string text:string entities:Vector<MessageEntity> document:flags.1?Document url:flags.2?string sticker:flags.3?Document = help.AppUpdate;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **can_not_skip** | [`flags.0?true`](type/true) | Unskippable, the new info must be shown to the user (with a popup or something else) |
| <mark>id</mark> | [`int`](type/int) | Update ID |
| <mark>version</mark> | [`string`](type/string) | New version name |
| <mark>text</mark> | [`string`](type/string) | Text description of the update |
| <mark>entities</mark> | [`Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **document** | [`flags.1?Document`](type/Document) | Application binary |
| **url** | [`flags.2?string`](type/string) | Application download URL |
| **sticker** | [`flags.3?Document`](type/Document) | Associated sticker |

---

## Type

[help.AppUpdate](type/help.AppUpdate)

---

## Example

```php
$helpAppUpdate = $client->help->appUpdate(
	can_not_skip : true,
	id : 57,
	version : 'e9whUoRqOfpKXyam',
	text : 'bQP1HiLTJocwzq0I',
	entities : array(
		$client->messageEntityUnknown(
			offset : 90,
			length : 89,
		),
		$client->messageEntityMention(
			offset : 90,
			length : 88,
		),
		$client->messageEntityHashtag(
			offset : 25,
			length : 63,
		),
		$client->messageEntityBotCommand(
			offset : 13,
			length : 93,
		),
		$client->messageEntityUrl(
			offset : 92,
			length : 5,
		),
		$client->messageEntityEmail(
			offset : 58,
			length : 30,
		),
		$client->messageEntityBold(
			offset : 43,
			length : 20,
		),
		$client->messageEntityItalic(
			offset : 27,
			length : 57,
		),
		$client->messageEntityCode(
			offset : 19,
			length : 0,
		),
		$client->messageEntityPre(
			offset : 81,
			length : 61,
			language : 'eI3yd1M4gx2jk6sb',
		),
		$client->messageEntityTextUrl(
			offset : 82,
			length : 50,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 80,
			length : 20,
			user_id : 1826367280316048510,
		),
		$client->inputMessageEntityMentionName(
			offset : 65,
			length : 80,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 46,
			length : 16,
		),
		$client->messageEntityCashtag(
			offset : 91,
			length : 3,
		),
		$client->messageEntityUnderline(
			offset : 11,
			length : 27,
		),
		$client->messageEntityStrike(
			offset : 45,
			length : 81,
		),
		$client->messageEntityBankCard(
			offset : 24,
			length : 24,
		),
		$client->messageEntitySpoiler(
			offset : 57,
			length : 73,
		),
		$client->messageEntityCustomEmoji(
			offset : 89,
			length : 7,
			document_id : -319677703039840940,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 68,
			length : 34,
		),
	),
	document : $client->documentEmpty(
		id : 5678105440759858514,
	),
	url : 'https://docs.liveproto.dev',
	sticker : $client->documentEmpty(
		id : -1011568881233135407,
	),
);
```