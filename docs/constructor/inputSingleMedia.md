# inputSingleMedia

**Description** : *A single media in an album or grouped media sent with messages.sendMultiMedia*

**Layer** : 211

```tl
inputSingleMedia#1cc6e91f flags:# media:InputMedia random_id:long message:string entities:flags.0?Vector<MessageEntity> = InputSingleMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>media</mark> | [`InputMedia`](type/InputMedia) | The media |
| <mark>random_id</mark> | [`long`](type/long) | Unique client media ID required to prevent message resending |
| <mark>message</mark> | [`string`](type/string) | A caption for the media |
| **entities** | [`flags.0?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Type

[InputSingleMedia](type/InputSingleMedia)

---

## Example

```php
$inputSingleMedia = $client->inputSingleMedia(
	media : $client->inputMediaEmpty(),
	random_id : -3934091878610116151,
	message : 'zAmbolcyHrjeY8Qn',
	entities : array(
		$client->messageEntityUnknown(
			offset : 86,
			length : 97,
		),
		$client->messageEntityMention(
			offset : 59,
			length : 44,
		),
		$client->messageEntityHashtag(
			offset : 42,
			length : 65,
		),
		$client->messageEntityBotCommand(
			offset : 24,
			length : 25,
		),
		$client->messageEntityUrl(
			offset : 19,
			length : 82,
		),
		$client->messageEntityEmail(
			offset : 22,
			length : 16,
		),
		$client->messageEntityBold(
			offset : 58,
			length : 57,
		),
		$client->messageEntityItalic(
			offset : 13,
			length : 55,
		),
		$client->messageEntityCode(
			offset : 66,
			length : 17,
		),
		$client->messageEntityPre(
			offset : 25,
			length : 62,
			language : 'bYjkvDZUScG8N0Js',
		),
		$client->messageEntityTextUrl(
			offset : 98,
			length : 21,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 56,
			length : 77,
			user_id : -523083709262305628,
		),
		$client->inputMessageEntityMentionName(
			offset : 65,
			length : 33,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 19,
			length : 80,
		),
		$client->messageEntityCashtag(
			offset : 82,
			length : 9,
		),
		$client->messageEntityUnderline(
			offset : 5,
			length : 9,
		),
		$client->messageEntityStrike(
			offset : 40,
			length : 52,
		),
		$client->messageEntityBankCard(
			offset : 98,
			length : 72,
		),
		$client->messageEntitySpoiler(
			offset : 81,
			length : 38,
		),
		$client->messageEntityCustomEmoji(
			offset : 62,
			length : 54,
			document_id : 5786009092379235374,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 39,
			length : 58,
		),
	),
);
```