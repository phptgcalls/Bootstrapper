# messages.getWebPagePreview

**Description** : *Get preview of webpage*

**Layer** : 211

```tl
messages.getWebPagePreview#570d6f6f flags:# message:string entities:flags.3?Vector<MessageEntity> = messages.WebPagePreview;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>message</mark> | [`string`](type/string) | Message from which to extract the preview |
| **entities** | [`flags.3?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Result

[messages.WebPagePreview](type/messages.WebPagePreview)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **ENTITY_BOUNDS_INVALID** | `400` | A specified entity offset or length is invalid, see here » for info on how to properly compute the entity offset/length |
| **MESSAGE_EMPTY** | `400` | The provided message is empty |

---

## Example

```php
$messagesWebPagePreview = $client->messages->getWebPagePreview(
	message : 'eMIQpqLWyKjhxt39',
	entities : array(
		$client->messageEntityUnknown(
			offset : 78,
			length : 40,
		),
		$client->messageEntityMention(
			offset : 19,
			length : 67,
		),
		$client->messageEntityHashtag(
			offset : 27,
			length : 4,
		),
		$client->messageEntityBotCommand(
			offset : 3,
			length : 21,
		),
		$client->messageEntityUrl(
			offset : 42,
			length : 23,
		),
		$client->messageEntityEmail(
			offset : 28,
			length : 87,
		),
		$client->messageEntityBold(
			offset : 24,
			length : 39,
		),
		$client->messageEntityItalic(
			offset : 27,
			length : 13,
		),
		$client->messageEntityCode(
			offset : 41,
			length : 79,
		),
		$client->messageEntityPre(
			offset : 38,
			length : 13,
			language : 'T8v9ClGYUcEsRNHQ',
		),
		$client->messageEntityTextUrl(
			offset : 79,
			length : 34,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 31,
			length : 68,
			user_id : 448201613494027978,
		),
		$client->inputMessageEntityMentionName(
			offset : 12,
			length : 67,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 5,
			length : 44,
		),
		$client->messageEntityCashtag(
			offset : 25,
			length : 54,
		),
		$client->messageEntityUnderline(
			offset : 87,
			length : 86,
		),
		$client->messageEntityStrike(
			offset : 7,
			length : 76,
		),
		$client->messageEntityBankCard(
			offset : 48,
			length : 69,
		),
		$client->messageEntitySpoiler(
			offset : 90,
			length : 17,
		),
		$client->messageEntityCustomEmoji(
			offset : 32,
			length : 80,
			document_id : 3706375523845674562,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 16,
			length : 25,
		),
	),
);
```