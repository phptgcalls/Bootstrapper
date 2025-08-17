# inputReplyToMessage

**Description** : *Reply to a message*

**Layer** : 211

```tl
inputReplyToMessage#869fbe10 flags:# reply_to_msg_id:int top_msg_id:flags.0?int reply_to_peer_id:flags.1?InputPeer quote_text:flags.2?string quote_entities:flags.3?Vector<MessageEntity> quote_offset:flags.4?int monoforum_peer_id:flags.5?InputPeer todo_item_id:flags.6?int = InputReplyTo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>reply_to_msg_id</mark> | [`int`](type/int) | The message ID to reply to |
| **top_msg_id** | [`flags.0?int`](type/int) | This field must contain the topic ID only when replying to messages in forum topics different from the "General" topic (i.e. reply_to_msg_id is set and reply_to_msg_id != topicID and topicID != 1).  If the replied-to message is deleted before the method finishes execution, the value in this field will be used to send the message to the correct topic, instead of the "General" topic |
| **reply_to_peer_id** | [`flags.1?InputPeer`](type/InputPeer) | Used to reply to messages sent to another chat (specified here), can only be used for non-protected chats and messages |
| **quote_text** | [`flags.2?string`](type/string) | Used to quote-reply to only a certain section (specified here) of the original message. The maximum UTF-8 length for quotes is specified in the quote_length_max config key |
| **quote_entities** | [`flags.3?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text from the quote_text field |
| **quote_offset** | [`flags.4?int`](type/int) | Offset of the message quote_text within the original message (in UTF-16 code units) |
| **monoforum_peer_id** | [`flags.5?InputPeer`](type/InputPeer) | NOTHING |
| **todo_item_id** | [`flags.6?int`](type/int) | NOTHING |

---

## Type

[InputReplyTo](type/InputReplyTo)

---

## Example

```php
$inputReplyTo = $client->inputReplyToMessage(
	reply_to_msg_id : 15,
	top_msg_id : 53,
	reply_to_peer_id : $client->inputPeerEmpty(),
	quote_text : 'uZB9ls62UEqMkvNh',
	quote_entities : array(
		$client->messageEntityUnknown(
			offset : 85,
			length : 8,
		),
		$client->messageEntityMention(
			offset : 21,
			length : 38,
		),
		$client->messageEntityHashtag(
			offset : 58,
			length : 91,
		),
		$client->messageEntityBotCommand(
			offset : 51,
			length : 100,
		),
		$client->messageEntityUrl(
			offset : 40,
			length : 10,
		),
		$client->messageEntityEmail(
			offset : 86,
			length : 79,
		),
		$client->messageEntityBold(
			offset : 33,
			length : 4,
		),
		$client->messageEntityItalic(
			offset : 62,
			length : 51,
		),
		$client->messageEntityCode(
			offset : 12,
			length : 44,
		),
		$client->messageEntityPre(
			offset : 45,
			length : 35,
			language : '4YOkPnD6ZQu1jqeC',
		),
		$client->messageEntityTextUrl(
			offset : 17,
			length : 52,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 39,
			length : 34,
			user_id : 3454779604684827448,
		),
		$client->inputMessageEntityMentionName(
			offset : 94,
			length : 77,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 54,
			length : 55,
		),
		$client->messageEntityCashtag(
			offset : 56,
			length : 42,
		),
		$client->messageEntityUnderline(
			offset : 92,
			length : 85,
		),
		$client->messageEntityStrike(
			offset : 44,
			length : 40,
		),
		$client->messageEntityBankCard(
			offset : 26,
			length : 35,
		),
		$client->messageEntitySpoiler(
			offset : 38,
			length : 74,
		),
		$client->messageEntityCustomEmoji(
			offset : 33,
			length : 59,
			document_id : 9185644692793164592,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 69,
			length : 13,
		),
	),
	quote_offset : 49,
	monoforum_peer_id : $client->inputPeerEmpty(),
	todo_item_id : 22,
);
```