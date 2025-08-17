# help.deepLinkInfo

**Description** : *Deep link info, see the here for more details*

**Layer** : 211

```tl
help.deepLinkInfo#6a4ee832 flags:# update_app:flags.0?true message:string entities:flags.1?Vector<MessageEntity> = help.DeepLinkInfo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **update_app** | [`flags.0?true`](type/true) | An update of the app is required to parse this link |
| <mark>message</mark> | [`string`](type/string) | Message to show to the user |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Type

[help.DeepLinkInfo](type/help.DeepLinkInfo)

---

## Example

```php
$helpDeepLinkInfo = $client->help->deepLinkInfo(
	update_app : true,
	message : 'EQrdHWBU2a4DcC8J',
	entities : array(
		$client->messageEntityUnknown(
			offset : 55,
			length : 72,
		),
		$client->messageEntityMention(
			offset : 64,
			length : 69,
		),
		$client->messageEntityHashtag(
			offset : 46,
			length : 82,
		),
		$client->messageEntityBotCommand(
			offset : 63,
			length : 60,
		),
		$client->messageEntityUrl(
			offset : 60,
			length : 42,
		),
		$client->messageEntityEmail(
			offset : 87,
			length : 45,
		),
		$client->messageEntityBold(
			offset : 15,
			length : 21,
		),
		$client->messageEntityItalic(
			offset : 68,
			length : 29,
		),
		$client->messageEntityCode(
			offset : 61,
			length : 54,
		),
		$client->messageEntityPre(
			offset : 84,
			length : 46,
			language : 'SrpIXC7UHbdk6oFs',
		),
		$client->messageEntityTextUrl(
			offset : 13,
			length : 11,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 74,
			length : 38,
			user_id : 1768151345586537958,
		),
		$client->inputMessageEntityMentionName(
			offset : 5,
			length : 35,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 27,
			length : 70,
		),
		$client->messageEntityCashtag(
			offset : 48,
			length : 19,
		),
		$client->messageEntityUnderline(
			offset : 48,
			length : 81,
		),
		$client->messageEntityStrike(
			offset : 76,
			length : 30,
		),
		$client->messageEntityBankCard(
			offset : 86,
			length : 79,
		),
		$client->messageEntitySpoiler(
			offset : 50,
			length : 20,
		),
		$client->messageEntityCustomEmoji(
			offset : 19,
			length : 0,
			document_id : -8743031212435878067,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 22,
			length : 0,
		),
	),
);
```