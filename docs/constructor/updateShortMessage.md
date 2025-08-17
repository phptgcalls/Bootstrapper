# updateShortMessage

**Description** : *Info about a message sent to (received from) another user*

**Layer** : 211

```tl
updateShortMessage#313bc7f8 flags:# out:flags.1?true mentioned:flags.4?true media_unread:flags.5?true silent:flags.13?true id:int user_id:long message:string pts:int pts_count:int date:int fwd_from:flags.2?MessageFwdHeader via_bot_id:flags.11?long reply_to:flags.3?MessageReplyHeader entities:flags.7?Vector<MessageEntity> ttl_period:flags.25?int = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **out** | [`flags.1?true`](type/true) | Whether the message is outgoing |
| **mentioned** | [`flags.4?true`](type/true) | Whether we were mentioned in the message |
| **media_unread** | [`flags.5?true`](type/true) | Whether there are some unread mentions in this message |
| **silent** | [`flags.13?true`](type/true) | If true, the message is a silent message, no notifications should be triggered |
| <mark>id</mark> | [`int`](type/int) | The message ID |
| <mark>user_id</mark> | [`long`](type/long) | The ID of the sender (if outgoing will be the ID of the destination) of the message |
| <mark>message</mark> | [`string`](type/string) | The message |
| <mark>pts</mark> | [`int`](type/int) | PTS |
| <mark>pts_count</mark> | [`int`](type/int) | PTS count |
| <mark>date</mark> | [`int`](type/int) | date |
| **fwd_from** | [`flags.2?MessageFwdHeader`](type/MessageFwdHeader) | Info about a forwarded message |
| **via_bot_id** | [`flags.11?long`](type/long) | Info about the inline bot used to generate this message |
| **reply_to** | [`flags.3?MessageReplyHeader`](type/MessageReplyHeader) | Reply and thread information |
| **entities** | [`flags.7?Vector<MessageEntity>`](type/MessageEntity) | Entities for styled text |
| **ttl_period** | [`flags.25?int`](type/int) | Time To Live of the message, once message.date+message.ttl_period === time(), the message will be deleted on the server, and must be deleted locally as well |

---

## Type

[Updates](type/Updates)

---

## Example

```php
$updates = $client->updateShortMessage(
	out : true,
	mentioned : true,
	media_unread : true,
	silent : true,
	id : 70,
	user_id : 3285846093749628973,
	message : '5yK9cOpkqDWR2muv',
	pts : 95,
	pts_count : 95,
	date : 45,
	fwd_from : $client->messageFwdHeader(
		imported : true,
		saved_out : true,
		from_id : $client->peerUser(
			user_id : 474294239723701834,
		),
		from_name : '5Iu9rPXnFyEh8KLM',
		date : 0,
		channel_post : 99,
		post_author : 'GwERgQnme3CBzjfJ',
		saved_from_peer : $client->peerUser(
			user_id : -7406580771434954707,
		),
		saved_from_msg_id : 94,
		saved_from_id : $client->peerUser(
			user_id : 7115592356958630253,
		),
		saved_from_name : 'DSYC1l7VmRZndWoH',
		saved_date : 31,
		psa_type : '2nrfNyAucvJl9eMS',
	),
	via_bot_id : 2142802985142436328,
	reply_to : $client->messageReplyHeader(
		reply_to_scheduled : true,
		forum_topic : true,
		quote : true,
		reply_to_msg_id : 76,
		reply_to_peer_id : $client->peerUser(
			user_id : 2560908516479683960,
		),
		reply_from : $client->messageFwdHeader(
			imported : true,
			saved_out : true,
			from_id : $client->peerUser(...),
			from_name : 'l0AQW6zGV89gThi4',
			date : 45,
			channel_post : 16,
			post_author : '6JeZGFw5Uiu2joNp',
			saved_from_peer : $client->peerUser(...),
			saved_from_msg_id : 42,
			saved_from_id : $client->peerUser(...),
			saved_from_name : 'HwlMr8zO4pn5xqef',
			saved_date : 30,
			psa_type : '6QiTI0cY4Dn2Gwve',
		),
		reply_media : $client->messageMediaEmpty(),
		reply_to_top_id : 23,
		quote_text : 'yVuaUo4dzGx0m5qC',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 92,
				length : 67,
			),
			$client->messageEntityMention(
				offset : 9,
				length : 43,
			),
			$client->messageEntityHashtag(
				offset : 64,
				length : 2,
			),
			$client->messageEntityBotCommand(
				offset : 72,
				length : 66,
			),
			$client->messageEntityUrl(
				offset : 87,
				length : 29,
			),
			$client->messageEntityEmail(
				offset : 9,
				length : 30,
			),
			$client->messageEntityBold(
				offset : 31,
				length : 32,
			),
			$client->messageEntityItalic(
				offset : 90,
				length : 51,
			),
			$client->messageEntityCode(
				offset : 38,
				length : 11,
			),
			$client->messageEntityPre(
				offset : 34,
				length : 72,
				language : 'McBCKa5VtXwvI9Fk',
			),
			$client->messageEntityTextUrl(
				offset : 71,
				length : 83,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 84,
				length : 95,
				user_id : 3104658027981516795,
			),
			$client->inputMessageEntityMentionName(
				offset : 98,
				length : 51,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 87,
				length : 68,
			),
			$client->messageEntityCashtag(
				offset : 82,
				length : 39,
			),
			$client->messageEntityUnderline(
				offset : 86,
				length : 11,
			),
			$client->messageEntityStrike(
				offset : 50,
				length : 7,
			),
			$client->messageEntityBankCard(
				offset : 5,
				length : 92,
			),
			$client->messageEntitySpoiler(
				offset : 52,
				length : 3,
			),
			$client->messageEntityCustomEmoji(
				offset : 89,
				length : 66,
				document_id : 1428831689388396490,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 46,
				length : 96,
			),
		),
		quote_offset : 81,
		todo_item_id : 13,
	),
	entities : array(
		$client->messageEntityUnknown(
			offset : 87,
			length : 57,
		),
		$client->messageEntityMention(
			offset : 41,
			length : 67,
		),
		$client->messageEntityHashtag(
			offset : 22,
			length : 82,
		),
		$client->messageEntityBotCommand(
			offset : 87,
			length : 60,
		),
		$client->messageEntityUrl(
			offset : 21,
			length : 18,
		),
		$client->messageEntityEmail(
			offset : 69,
			length : 57,
		),
		$client->messageEntityBold(
			offset : 86,
			length : 70,
		),
		$client->messageEntityItalic(
			offset : 3,
			length : 22,
		),
		$client->messageEntityCode(
			offset : 14,
			length : 72,
		),
		$client->messageEntityPre(
			offset : 16,
			length : 76,
			language : 'SAclG4gHMPREubV2',
		),
		$client->messageEntityTextUrl(
			offset : 68,
			length : 46,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 45,
			length : 59,
			user_id : -5106863161608062798,
		),
		$client->inputMessageEntityMentionName(
			offset : 2,
			length : 12,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 48,
			length : 14,
		),
		$client->messageEntityCashtag(
			offset : 60,
			length : 82,
		),
		$client->messageEntityUnderline(
			offset : 49,
			length : 51,
		),
		$client->messageEntityStrike(
			offset : 42,
			length : 57,
		),
		$client->messageEntityBankCard(
			offset : 83,
			length : 78,
		),
		$client->messageEntitySpoiler(
			offset : 68,
			length : 81,
		),
		$client->messageEntityCustomEmoji(
			offset : 88,
			length : 22,
			document_id : 6403422614320385548,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 67,
			length : 70,
		),
	),
	ttl_period : 1,
);
```