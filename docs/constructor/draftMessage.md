# draftMessage

**Description** : *Represents a message draft*

**Layer** : 211

```tl
draftMessage#96eaa5eb flags:# no_webpage:flags.1?true invert_media:flags.6?true reply_to:flags.4?InputReplyTo message:string entities:flags.3?Vector<MessageEntity> media:flags.5?InputMedia date:int effect:flags.7?long suggested_post:flags.8?SuggestedPost = DraftMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **no_webpage** | [`flags.1?true`](type/true) | Whether no webpage preview will be generated |
| **invert_media** | [`flags.6?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| **reply_to** | [`flags.4?InputReplyTo`](type/InputReplyTo) | If set, indicates that the message should be sent in reply to the specified message or story |
| <mark>message</mark> | [`string`](type/string) | The draft |
| **entities** | [`flags.3?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **media** | [`flags.5?InputMedia`](type/InputMedia) | Media |
| <mark>date</mark> | [`int`](type/int) | Date of last update of the draft |
| **effect** | [`flags.7?long`](type/long) | A message effect that should be played as specified here » |
| **suggested_post** | [`flags.8?SuggestedPost`](type/SuggestedPost) | NOTHING |

---

## Type

[DraftMessage](type/DraftMessage)

---

## Example

```php
$draftMessage = $client->draftMessage(
	no_webpage : true,
	invert_media : true,
	reply_to : $client->inputReplyToMessage(
		reply_to_msg_id : 57,
		top_msg_id : 29,
		reply_to_peer_id : $client->inputPeerEmpty(),
		quote_text : 'Ut147M0RQVY58rqA',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 77,
				length : 9,
			),
			$client->messageEntityMention(
				offset : 36,
				length : 8,
			),
			$client->messageEntityHashtag(
				offset : 45,
				length : 89,
			),
			$client->messageEntityBotCommand(
				offset : 50,
				length : 59,
			),
			$client->messageEntityUrl(
				offset : 70,
				length : 35,
			),
			$client->messageEntityEmail(
				offset : 5,
				length : 60,
			),
			$client->messageEntityBold(
				offset : 88,
				length : 52,
			),
			$client->messageEntityItalic(
				offset : 66,
				length : 100,
			),
			$client->messageEntityCode(
				offset : 97,
				length : 5,
			),
			$client->messageEntityPre(
				offset : 87,
				length : 21,
				language : 'SCtKl9Yo85B6Txgh',
			),
			$client->messageEntityTextUrl(
				offset : 48,
				length : 43,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 48,
				length : 14,
				user_id : -1625917586764080845,
			),
			$client->inputMessageEntityMentionName(
				offset : 3,
				length : 80,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 0,
				length : 21,
			),
			$client->messageEntityCashtag(
				offset : 81,
				length : 10,
			),
			$client->messageEntityUnderline(
				offset : 35,
				length : 82,
			),
			$client->messageEntityStrike(
				offset : 63,
				length : 22,
			),
			$client->messageEntityBankCard(
				offset : 33,
				length : 62,
			),
			$client->messageEntitySpoiler(
				offset : 94,
				length : 74,
			),
			$client->messageEntityCustomEmoji(
				offset : 84,
				length : 73,
				document_id : -1742461888635405648,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 67,
				length : 58,
			),
		),
		quote_offset : 94,
		monoforum_peer_id : $client->inputPeerEmpty(),
		todo_item_id : 16,
	),
	message : '62GhTXUwBaPqpZJg',
	entities : array(
		$client->messageEntityUnknown(
			offset : 46,
			length : 35,
		),
		$client->messageEntityMention(
			offset : 16,
			length : 69,
		),
		$client->messageEntityHashtag(
			offset : 59,
			length : 44,
		),
		$client->messageEntityBotCommand(
			offset : 47,
			length : 7,
		),
		$client->messageEntityUrl(
			offset : 19,
			length : 26,
		),
		$client->messageEntityEmail(
			offset : 31,
			length : 86,
		),
		$client->messageEntityBold(
			offset : 76,
			length : 81,
		),
		$client->messageEntityItalic(
			offset : 61,
			length : 29,
		),
		$client->messageEntityCode(
			offset : 34,
			length : 87,
		),
		$client->messageEntityPre(
			offset : 25,
			length : 75,
			language : '0Nbon63Y2B5DarpE',
		),
		$client->messageEntityTextUrl(
			offset : 47,
			length : 82,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 2,
			length : 40,
			user_id : -5814028304174895562,
		),
		$client->inputMessageEntityMentionName(
			offset : 13,
			length : 45,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 36,
			length : 8,
		),
		$client->messageEntityCashtag(
			offset : 49,
			length : 13,
		),
		$client->messageEntityUnderline(
			offset : 34,
			length : 71,
		),
		$client->messageEntityStrike(
			offset : 94,
			length : 14,
		),
		$client->messageEntityBankCard(
			offset : 22,
			length : 22,
		),
		$client->messageEntitySpoiler(
			offset : 10,
			length : 47,
		),
		$client->messageEntityCustomEmoji(
			offset : 38,
			length : 38,
			document_id : -5197618359068644148,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 99,
			length : 39,
		),
	),
	media : $client->inputMediaEmpty(),
	date : 91,
	effect : 8186751341637955690,
	suggested_post : $client->suggestedPost(
		accepted : true,
		rejected : true,
		price : $client->starsAmount(
			amount : -3970742873734817902,
			nanos : 61,
		),
		schedule_date : 10,
	),
);
```