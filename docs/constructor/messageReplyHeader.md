# messageReplyHeader

**Description** : *Message replies and thread information*

**Layer** : 211

```tl
messageReplyHeader#6917560b flags:# reply_to_scheduled:flags.2?true forum_topic:flags.3?true quote:flags.9?true reply_to_msg_id:flags.4?int reply_to_peer_id:flags.0?Peer reply_from:flags.5?MessageFwdHeader reply_media:flags.8?MessageMedia reply_to_top_id:flags.1?int quote_text:flags.6?string quote_entities:flags.7?Vector<MessageEntity> quote_offset:flags.10?int todo_item_id:flags.11?int = MessageReplyHeader;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **reply_to_scheduled** | [`flags.2?true`](type/true) | This is a reply to a scheduled message |
| **forum_topic** | [`flags.3?true`](type/true) | Whether this message was sent in a forum topic (except for the General topic) |
| **quote** | [`flags.9?true`](type/true) | Whether this message is quoting a part of another message |
| **reply_to_msg_id** | [`flags.4?int`](type/int) | ID of message to which this message is replying |
| **reply_to_peer_id** | [`flags.0?Peer`](type/Peer) | For replies sent in channel discussion threads of which the current user is not a member, the discussion group ID |
| **reply_from** | [`flags.5?MessageFwdHeader`](type/MessageFwdHeader) | When replying to a message sent by a certain peer to another chat, contains info about the peer that originally sent the message to that other chat |
| **reply_media** | [`flags.8?MessageMedia`](type/MessageMedia) | When replying to a media sent by a certain peer to another chat, contains the media of the replied-to message |
| **reply_to_top_id** | [`flags.1?int`](type/int) | ID of the message that started this message thread |
| **quote_text** | [`flags.6?string`](type/string) | Used to quote-reply to only a certain section (specified here) of the original message |
| **quote_entities** | [`flags.7?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text from the quote_text field |
| **quote_offset** | [`flags.10?int`](type/int) | Offset of the message quote_text within the original message (in UTF-16 code units) |
| **todo_item_id** | [`flags.11?int`](type/int) | NOTHING |

---

## Type

[MessageReplyHeader](type/MessageReplyHeader)

---

## Example

```php
$messageReplyHeader = $client->messageReplyHeader(
	reply_to_scheduled : true,
	forum_topic : true,
	quote : true,
	reply_to_msg_id : 5,
	reply_to_peer_id : $client->peerUser(
		user_id : -5526831493540709596,
	),
	reply_from : $client->messageFwdHeader(
		imported : true,
		saved_out : true,
		from_id : $client->peerUser(
			user_id : -7375600627673910767,
		),
		from_name : '6KrdqQhiAaSnC1gP',
		date : 36,
		channel_post : 15,
		post_author : 'noyYqaDBC0tPMfS1',
		saved_from_peer : $client->peerUser(
			user_id : -621192761996092192,
		),
		saved_from_msg_id : 46,
		saved_from_id : $client->peerUser(
			user_id : -7980369492705833222,
		),
		saved_from_name : 'Yc2xi6TaZM7CuHbA',
		saved_date : 44,
		psa_type : 'GsYSwhVr3vm49OoR',
	),
	reply_media : $client->messageMediaEmpty(),
	reply_to_top_id : 46,
	quote_text : 'u5Obp4HF3kLNlG7X',
	quote_entities : array(
		$client->messageEntityUnknown(
			offset : 53,
			length : 8,
		),
		$client->messageEntityMention(
			offset : 4,
			length : 4,
		),
		$client->messageEntityHashtag(
			offset : 99,
			length : 46,
		),
		$client->messageEntityBotCommand(
			offset : 94,
			length : 31,
		),
		$client->messageEntityUrl(
			offset : 49,
			length : 74,
		),
		$client->messageEntityEmail(
			offset : 88,
			length : 88,
		),
		$client->messageEntityBold(
			offset : 45,
			length : 88,
		),
		$client->messageEntityItalic(
			offset : 71,
			length : 64,
		),
		$client->messageEntityCode(
			offset : 99,
			length : 8,
		),
		$client->messageEntityPre(
			offset : 79,
			length : 76,
			language : 'Ed39LX5jpegOCD8o',
		),
		$client->messageEntityTextUrl(
			offset : 63,
			length : 12,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 33,
			length : 15,
			user_id : 7389295540107825552,
		),
		$client->inputMessageEntityMentionName(
			offset : 13,
			length : 62,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 55,
			length : 45,
		),
		$client->messageEntityCashtag(
			offset : 55,
			length : 63,
		),
		$client->messageEntityUnderline(
			offset : 71,
			length : 98,
		),
		$client->messageEntityStrike(
			offset : 3,
			length : 95,
		),
		$client->messageEntityBankCard(
			offset : 59,
			length : 51,
		),
		$client->messageEntitySpoiler(
			offset : 29,
			length : 76,
		),
		$client->messageEntityCustomEmoji(
			offset : 44,
			length : 56,
			document_id : 6829936043037580535,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 69,
			length : 47,
		),
	),
	quote_offset : 12,
	todo_item_id : 64,
);
```