# messages.saveDraft

**Description** : *Save a message draft associated to a chat*

**Layer** : 211

```tl
messages.saveDraft#54ae308e flags:# no_webpage:flags.1?true invert_media:flags.6?true reply_to:flags.4?InputReplyTo peer:InputPeer message:string entities:flags.3?Vector<MessageEntity> media:flags.5?InputMedia effect:flags.7?long suggested_post:flags.8?SuggestedPost = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **no_webpage** | [`flags.1?true`](type/true) | Disable generation of the webpage preview |
| **invert_media** | [`flags.6?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| **reply_to** | [`flags.4?InputReplyTo`](type/InputReplyTo) | If set, indicates that the message should be sent in reply to the specified message or story |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Destination of the message that should be sent |
| <mark>message</mark> | [`string`](type/string) | The draft |
| **entities** | [`flags.3?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **media** | [`flags.5?InputMedia`](type/InputMedia) | Attached media |
| **effect** | [`flags.7?long`](type/long) | Specifies a message effect » to use for the message |
| **suggested_post** | [`flags.8?SuggestedPost`](type/SuggestedPost) | NOTHING |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **ENTITY_BOUNDS_INVALID** | `400` | A specified entity offset or length is invalid, see here » for info on how to properly compute the entity offset/length |
| **MSG_ID_INVALID** | `400` | Invalid message ID provided |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$bool = $client->messages->saveDraft(
	no_webpage : true,
	invert_media : true,
	reply_to : $client->inputReplyToMessage(
		reply_to_msg_id : 60,
		top_msg_id : 94,
		reply_to_peer_id : $client->inputPeerEmpty(),
		quote_text : 'K7d4VXpgEIf6bZ2Y',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 79,
				length : 37,
			),
			$client->messageEntityMention(
				offset : 0,
				length : 98,
			),
			$client->messageEntityHashtag(
				offset : 19,
				length : 34,
			),
			$client->messageEntityBotCommand(
				offset : 14,
				length : 64,
			),
			$client->messageEntityUrl(
				offset : 96,
				length : 33,
			),
			$client->messageEntityEmail(
				offset : 20,
				length : 67,
			),
			$client->messageEntityBold(
				offset : 40,
				length : 4,
			),
			$client->messageEntityItalic(
				offset : 3,
				length : 69,
			),
			$client->messageEntityCode(
				offset : 61,
				length : 67,
			),
			$client->messageEntityPre(
				offset : 95,
				length : 99,
				language : 'A4vTMJ7IazmCVGSB',
			),
			$client->messageEntityTextUrl(
				offset : 37,
				length : 0,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 11,
				length : 68,
				user_id : -3501333518489590281,
			),
			$client->inputMessageEntityMentionName(
				offset : 69,
				length : 65,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 74,
				length : 51,
			),
			$client->messageEntityCashtag(
				offset : 73,
				length : 71,
			),
			$client->messageEntityUnderline(
				offset : 91,
				length : 22,
			),
			$client->messageEntityStrike(
				offset : 95,
				length : 45,
			),
			$client->messageEntityBankCard(
				offset : 7,
				length : 68,
			),
			$client->messageEntitySpoiler(
				offset : 54,
				length : 60,
			),
			$client->messageEntityCustomEmoji(
				offset : 65,
				length : 44,
				document_id : -7730161752195510433,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 17,
				length : 17,
			),
		),
		quote_offset : 36,
		monoforum_peer_id : $client->inputPeerEmpty(),
		todo_item_id : 63,
	),
	peer : $client->inputPeerEmpty(),
	message : 's6gIntb1fQwhYSkZ',
	entities : array(
		$client->messageEntityUnknown(
			offset : 31,
			length : 0,
		),
		$client->messageEntityMention(
			offset : 59,
			length : 47,
		),
		$client->messageEntityHashtag(
			offset : 48,
			length : 52,
		),
		$client->messageEntityBotCommand(
			offset : 86,
			length : 25,
		),
		$client->messageEntityUrl(
			offset : 83,
			length : 16,
		),
		$client->messageEntityEmail(
			offset : 93,
			length : 90,
		),
		$client->messageEntityBold(
			offset : 10,
			length : 33,
		),
		$client->messageEntityItalic(
			offset : 82,
			length : 92,
		),
		$client->messageEntityCode(
			offset : 76,
			length : 26,
		),
		$client->messageEntityPre(
			offset : 4,
			length : 18,
			language : '4YSRLk5HXKod81t9',
		),
		$client->messageEntityTextUrl(
			offset : 80,
			length : 1,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 80,
			length : 41,
			user_id : 7598013706549743299,
		),
		$client->inputMessageEntityMentionName(
			offset : 63,
			length : 5,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 33,
			length : 31,
		),
		$client->messageEntityCashtag(
			offset : 60,
			length : 81,
		),
		$client->messageEntityUnderline(
			offset : 85,
			length : 19,
		),
		$client->messageEntityStrike(
			offset : 87,
			length : 29,
		),
		$client->messageEntityBankCard(
			offset : 41,
			length : 81,
		),
		$client->messageEntitySpoiler(
			offset : 45,
			length : 93,
		),
		$client->messageEntityCustomEmoji(
			offset : 66,
			length : 5,
			document_id : -4618777184788750848,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 5,
			length : 57,
		),
	),
	media : $client->inputMediaEmpty(),
	effect : -3994626672806025943,
	suggested_post : $client->suggestedPost(
		accepted : true,
		rejected : true,
		price : $client->starsAmount(
			amount : 5385956798521945142,
			nanos : 13,
		),
		schedule_date : 40,
	),
);
```