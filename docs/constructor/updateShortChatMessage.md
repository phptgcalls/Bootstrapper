# updateShortChatMessage

**Description** : *Shortened constructor containing info on one new incoming text message from a chat*

**Layer** : 211

```tl
updateShortChatMessage#4d6deea5 flags:# out:flags.1?true mentioned:flags.4?true media_unread:flags.5?true silent:flags.13?true id:int from_id:long chat_id:long message:string pts:int pts_count:int date:int fwd_from:flags.2?MessageFwdHeader via_bot_id:flags.11?long reply_to:flags.3?MessageReplyHeader entities:flags.7?Vector<MessageEntity> ttl_period:flags.25?int = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **out** | [`flags.1?true`](type/true) | Whether the message is outgoing |
| **mentioned** | [`flags.4?true`](type/true) | Whether we were mentioned in this message |
| **media_unread** | [`flags.5?true`](type/true) | Whether the message contains some unread mentions |
| **silent** | [`flags.13?true`](type/true) | If true, the message is a silent message, no notifications should be triggered |
| <mark>id</mark> | [`int`](type/int) | ID of the message |
| <mark>from_id</mark> | [`long`](type/long) | ID of the sender of the message |
| <mark>chat_id</mark> | [`long`](type/long) | ID of the chat where the message was sent |
| <mark>message</mark> | [`string`](type/string) | Message |
| <mark>pts</mark> | [`int`](type/int) | PTS |
| <mark>pts_count</mark> | [`int`](type/int) | PTS count |
| <mark>date</mark> | [`int`](type/int) | date |
| **fwd_from** | [`flags.2?MessageFwdHeader`](type/MessageFwdHeader) | Info about a forwarded message |
| **via_bot_id** | [`flags.11?long`](type/long) | Info about the inline bot used to generate this message |
| **reply_to** | [`flags.3?MessageReplyHeader`](type/MessageReplyHeader) | Reply (thread) information |
| **entities** | [`flags.7?Vector<MessageEntity>`](type/MessageEntity) | Entities for styled text |
| **ttl_period** | [`flags.25?int`](type/int) | Time To Live of the message, once updateShortChatMessage.date+updateShortChatMessage.ttl_period === time(), the message will be deleted on the server, and must be deleted locally as well |

---

## Type

[Updates](type/Updates)

---

## Example

```php
$updates = $client->updateShortChatMessage(
	out : true,
	mentioned : true,
	media_unread : true,
	silent : true,
	id : 90,
	from_id : -5061239861875273995,
	chat_id : 3496672638192321723,
	message : 'OsNELUS0XDIaMeVR',
	pts : 100,
	pts_count : 5,
	date : 92,
	fwd_from : $client->messageFwdHeader(
		imported : true,
		saved_out : true,
		from_id : $client->peerUser(
			user_id : -6730117762344600997,
		),
		from_name : 'weRhiVjuJm5OIA1P',
		date : 22,
		channel_post : 21,
		post_author : 'ocrkxmYauifDM26I',
		saved_from_peer : $client->peerUser(
			user_id : 8787646347023099502,
		),
		saved_from_msg_id : 16,
		saved_from_id : $client->peerUser(
			user_id : 2188324091451099561,
		),
		saved_from_name : 'zCjfOB97UHGrL1sA',
		saved_date : 9,
		psa_type : 'PlHmyAQXvDwdEMBp',
	),
	via_bot_id : -1821179168599545317,
	reply_to : $client->messageReplyHeader(
		reply_to_scheduled : true,
		forum_topic : true,
		quote : true,
		reply_to_msg_id : 98,
		reply_to_peer_id : $client->peerUser(
			user_id : 259865931455481594,
		),
		reply_from : $client->messageFwdHeader(
			imported : true,
			saved_out : true,
			from_id : $client->peerUser(...),
			from_name : 'OcD2ZFr5WBbXVoqy',
			date : 91,
			channel_post : 25,
			post_author : 'qUxLlr5iQ8yVvzjK',
			saved_from_peer : $client->peerUser(...),
			saved_from_msg_id : 35,
			saved_from_id : $client->peerUser(...),
			saved_from_name : '8tbnRWal5jJPE7Zf',
			saved_date : 56,
			psa_type : 'XQBkA9N6fIxHGJ7c',
		),
		reply_media : $client->messageMediaEmpty(),
		reply_to_top_id : 66,
		quote_text : '5v3FdLUATPkjSDlY',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 99,
				length : 53,
			),
			$client->messageEntityMention(
				offset : 67,
				length : 23,
			),
			$client->messageEntityHashtag(
				offset : 57,
				length : 5,
			),
			$client->messageEntityBotCommand(
				offset : 7,
				length : 31,
			),
			$client->messageEntityUrl(
				offset : 55,
				length : 83,
			),
			$client->messageEntityEmail(
				offset : 62,
				length : 68,
			),
			$client->messageEntityBold(
				offset : 4,
				length : 43,
			),
			$client->messageEntityItalic(
				offset : 12,
				length : 8,
			),
			$client->messageEntityCode(
				offset : 74,
				length : 71,
			),
			$client->messageEntityPre(
				offset : 57,
				length : 14,
				language : 'hJRAUlIMLzpQ3sZj',
			),
			$client->messageEntityTextUrl(
				offset : 16,
				length : 41,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 13,
				length : 82,
				user_id : 133913993925943050,
			),
			$client->inputMessageEntityMentionName(
				offset : 52,
				length : 71,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 44,
				length : 34,
			),
			$client->messageEntityCashtag(
				offset : 2,
				length : 19,
			),
			$client->messageEntityUnderline(
				offset : 81,
				length : 39,
			),
			$client->messageEntityStrike(
				offset : 3,
				length : 4,
			),
			$client->messageEntityBankCard(
				offset : 8,
				length : 70,
			),
			$client->messageEntitySpoiler(
				offset : 50,
				length : 95,
			),
			$client->messageEntityCustomEmoji(
				offset : 60,
				length : 54,
				document_id : -3229935940053864523,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 8,
				length : 21,
			),
		),
		quote_offset : 69,
		todo_item_id : 6,
	),
	entities : array(
		$client->messageEntityUnknown(
			offset : 84,
			length : 92,
		),
		$client->messageEntityMention(
			offset : 39,
			length : 86,
		),
		$client->messageEntityHashtag(
			offset : 33,
			length : 95,
		),
		$client->messageEntityBotCommand(
			offset : 28,
			length : 70,
		),
		$client->messageEntityUrl(
			offset : 62,
			length : 74,
		),
		$client->messageEntityEmail(
			offset : 43,
			length : 68,
		),
		$client->messageEntityBold(
			offset : 92,
			length : 55,
		),
		$client->messageEntityItalic(
			offset : 97,
			length : 80,
		),
		$client->messageEntityCode(
			offset : 41,
			length : 70,
		),
		$client->messageEntityPre(
			offset : 26,
			length : 11,
			language : 'uPdJgj5N7AaC4txO',
		),
		$client->messageEntityTextUrl(
			offset : 10,
			length : 37,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 93,
			length : 23,
			user_id : -7142953088366369814,
		),
		$client->inputMessageEntityMentionName(
			offset : 82,
			length : 42,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 25,
			length : 3,
		),
		$client->messageEntityCashtag(
			offset : 4,
			length : 46,
		),
		$client->messageEntityUnderline(
			offset : 60,
			length : 82,
		),
		$client->messageEntityStrike(
			offset : 35,
			length : 18,
		),
		$client->messageEntityBankCard(
			offset : 96,
			length : 6,
		),
		$client->messageEntitySpoiler(
			offset : 41,
			length : 12,
		),
		$client->messageEntityCustomEmoji(
			offset : 90,
			length : 76,
			document_id : 6603015653631351064,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 18,
			length : 8,
		),
	),
	ttl_period : 75,
);
```