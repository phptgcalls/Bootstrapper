# updateShortSentMessage

**Description** : *Shortened constructor containing info on one outgoing message to a contact (the destination chat has to be extracted from the method call that returned this object)*

**Layer** : 211

```tl
updateShortSentMessage#9015e101 flags:# out:flags.1?true id:int pts:int pts_count:int date:int media:flags.9?MessageMedia entities:flags.7?Vector<MessageEntity> ttl_period:flags.25?int = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **out** | [`flags.1?true`](type/true) | Whether the message is outgoing |
| <mark>id</mark> | [`int`](type/int) | ID of the sent message |
| <mark>pts</mark> | [`int`](type/int) | PTS |
| <mark>pts_count</mark> | [`int`](type/int) | PTS count |
| <mark>date</mark> | [`int`](type/int) | date |
| **media** | [`flags.9?MessageMedia`](type/MessageMedia) | Attached media |
| **entities** | [`flags.7?Vector<MessageEntity>`](type/MessageEntity) | Entities for styled text |
| **ttl_period** | [`flags.25?int`](type/int) | Time To Live of the message, once message.date+message.ttl_period === time(), the message will be deleted on the server, and must be deleted locally as well |

---

## Type

[Updates](type/Updates)

---

## Example

```php
$updates = $client->updateShortSentMessage(
	out : true,
	id : 16,
	pts : 93,
	pts_count : 34,
	date : 53,
	media : $client->messageMediaEmpty(),
	entities : array(
		$client->messageEntityUnknown(
			offset : 0,
			length : 39,
		),
		$client->messageEntityMention(
			offset : 79,
			length : 23,
		),
		$client->messageEntityHashtag(
			offset : 38,
			length : 36,
		),
		$client->messageEntityBotCommand(
			offset : 9,
			length : 46,
		),
		$client->messageEntityUrl(
			offset : 54,
			length : 8,
		),
		$client->messageEntityEmail(
			offset : 72,
			length : 49,
		),
		$client->messageEntityBold(
			offset : 31,
			length : 0,
		),
		$client->messageEntityItalic(
			offset : 15,
			length : 71,
		),
		$client->messageEntityCode(
			offset : 31,
			length : 6,
		),
		$client->messageEntityPre(
			offset : 50,
			length : 60,
			language : 'M2dsP3mVbnurHWeO',
		),
		$client->messageEntityTextUrl(
			offset : 60,
			length : 97,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 67,
			length : 47,
			user_id : 6623806092199670714,
		),
		$client->inputMessageEntityMentionName(
			offset : 18,
			length : 32,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 100,
			length : 85,
		),
		$client->messageEntityCashtag(
			offset : 87,
			length : 94,
		),
		$client->messageEntityUnderline(
			offset : 81,
			length : 100,
		),
		$client->messageEntityStrike(
			offset : 26,
			length : 18,
		),
		$client->messageEntityBankCard(
			offset : 94,
			length : 82,
		),
		$client->messageEntitySpoiler(
			offset : 94,
			length : 53,
		),
		$client->messageEntityCustomEmoji(
			offset : 26,
			length : 76,
			document_id : -279177997243733825,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 38,
			length : 2,
		),
	),
	ttl_period : 7,
);
```