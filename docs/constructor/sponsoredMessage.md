# sponsoredMessage

**Description** : *A sponsored message*

**Layer** : 211

```tl
sponsoredMessage#7dbf8673 flags:# recommended:flags.5?true can_report:flags.12?true random_id:bytes url:string title:string message:string entities:flags.1?Vector<MessageEntity> photo:flags.6?Photo media:flags.14?MessageMedia color:flags.13?PeerColor button_text:string sponsor_info:flags.7?string additional_info:flags.8?string min_display_duration:flags.15?int max_display_duration:flags.15?int = SponsoredMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **recommended** | [`flags.5?true`](type/true) | Whether the message needs to be labeled as "recommended" instead of "sponsored" |
| **can_report** | [`flags.12?true`](type/true) | Whether this message can be reported as specified here » |
| <mark>random_id</mark> | [`bytes`](type/bytes) | Message ID |
| <mark>url</mark> | [`string`](type/string) | Contains the URL to open when the user clicks on the sponsored message |
| <mark>title</mark> | [`string`](type/string) | Contains the title of the sponsored message |
| <mark>message</mark> | [`string`](type/string) | Sponsored message |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text in message |
| **photo** | [`flags.6?Photo`](type/Photo) | If set, contains a custom profile photo bubble that should be displayed for the sponsored message, like for messages sent in groups |
| **media** | [`flags.14?MessageMedia`](type/MessageMedia) | If set, contains some media |
| **color** | [`flags.13?PeerColor`](type/PeerColor) | If set, the sponsored message should use the message accent color » specified in color |
| <mark>button_text</mark> | [`string`](type/string) | Label of the sponsored message button |
| **sponsor_info** | [`flags.7?string`](type/string) | If set, contains additional information about the sponsor to be shown along with the message |
| **additional_info** | [`flags.8?string`](type/string) | If set, contains additional information about the sponsored message to be shown along with the message |
| **min_display_duration** | [`flags.15?int`](type/int) | NOTHING |
| **max_display_duration** | [`flags.15?int`](type/int) | NOTHING |

---

## Type

[SponsoredMessage](type/SponsoredMessage)

---

## Example

```php
$sponsoredMessage = $client->sponsoredMessage(
	recommended : true,
	can_report : true,
	random_id : '??_?LiveProto?%?',
	url : 'https://docs.liveproto.dev',
	title : 'CGde1MRk75P9AjlH',
	message : 'JaWfR145PQ8eAVmo',
	entities : array(
		$client->messageEntityUnknown(
			offset : 88,
			length : 3,
		),
		$client->messageEntityMention(
			offset : 25,
			length : 100,
		),
		$client->messageEntityHashtag(
			offset : 19,
			length : 66,
		),
		$client->messageEntityBotCommand(
			offset : 2,
			length : 21,
		),
		$client->messageEntityUrl(
			offset : 25,
			length : 90,
		),
		$client->messageEntityEmail(
			offset : 76,
			length : 75,
		),
		$client->messageEntityBold(
			offset : 32,
			length : 47,
		),
		$client->messageEntityItalic(
			offset : 79,
			length : 70,
		),
		$client->messageEntityCode(
			offset : 36,
			length : 79,
		),
		$client->messageEntityPre(
			offset : 57,
			length : 9,
			language : 'xTGytXYwBF8cgl3i',
		),
		$client->messageEntityTextUrl(
			offset : 89,
			length : 13,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 19,
			length : 26,
			user_id : 6515246358568585248,
		),
		$client->inputMessageEntityMentionName(
			offset : 85,
			length : 30,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 55,
			length : 30,
		),
		$client->messageEntityCashtag(
			offset : 43,
			length : 0,
		),
		$client->messageEntityUnderline(
			offset : 50,
			length : 1,
		),
		$client->messageEntityStrike(
			offset : 80,
			length : 66,
		),
		$client->messageEntityBankCard(
			offset : 86,
			length : 54,
		),
		$client->messageEntitySpoiler(
			offset : 20,
			length : 56,
		),
		$client->messageEntityCustomEmoji(
			offset : 30,
			length : 37,
			document_id : 7374204061429402449,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 45,
			length : 93,
		),
	),
	photo : $client->photoEmpty(
		id : 2516959683068565822,
	),
	media : $client->messageMediaEmpty(),
	color : $client->peerColor(
		color : 5,
		background_emoji_id : 7453788988547496618,
	),
	button_text : '9hgbJoE1OA2vzUeZ',
	sponsor_info : 'QE5v6noSgkPT7Ae2',
	additional_info : 'qz69SxDgbrQOLYIc',
	min_display_duration : 1,
	max_display_duration : 51,
);
```