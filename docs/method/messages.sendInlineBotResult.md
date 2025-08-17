# messages.sendInlineBotResult

**Description** : *Send a result obtained using messages.getInlineBotResults*

**Layer** : 211

```tl
messages.sendInlineBotResult#c0cf7646 flags:# silent:flags.5?true background:flags.6?true clear_draft:flags.7?true hide_via:flags.11?true peer:InputPeer reply_to:flags.0?InputReplyTo random_id:long query_id:long id:string schedule_date:flags.10?int send_as:flags.13?InputPeer quick_reply_shortcut:flags.17?InputQuickReplyShortcut allow_paid_stars:flags.21?long = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **silent** | [`flags.5?true`](type/true) | Whether to send the message silently (no notification will be triggered on the other client) |
| **background** | [`flags.6?true`](type/true) | Whether to send the message in background |
| **clear_draft** | [`flags.7?true`](type/true) | Whether to clear the draft |
| **hide_via** | [`flags.11?true`](type/true) | Whether to hide the via @botname in the resulting message (only for bot usernames encountered in the config) |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Destination |
| **reply_to** | [`flags.0?InputReplyTo`](type/InputReplyTo) | If set, indicates that the message should be sent in reply to the specified message or story |
| <mark>random_id</mark> | [`long`](type/long) | Random ID to avoid resending the same query |
| <mark>query_id</mark> | [`long`](type/long) | Query ID from messages.getInlineBotResults |
| <mark>id</mark> | [`string`](type/string) | Result ID from messages.getInlineBotResults |
| **schedule_date** | [`flags.10?int`](type/int) | Scheduled message date for scheduled messages |
| **send_as** | [`flags.13?InputPeer`](type/InputPeer) | Send this message as the specified peer |
| **quick_reply_shortcut** | [`flags.17?InputQuickReplyShortcut`](type/InputQuickReplyShortcut) | Add the message to the specified quick reply shortcut », instead |
| **allow_paid_stars** | [`flags.21?long`](type/long) | NOTHING |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHANNEL_INVALID** | `400` | The provided channel is invalid |
| **CHANNEL_PRIVATE** | `400` | You haven't joined this channel/supergroup |
| **CHAT_ADMIN_REQUIRED** | `400` | You must be an admin in this chat to do this |
| **CHAT_GUEST_SEND_FORBIDDEN** | `403` | You join the discussion group before commenting, see here » for more info |
| **CHAT_RESTRICTED** | `400` | You can't send messages in this chat, you were restricted |
| **CHAT_SEND_AUDIOS_FORBIDDEN** | `403` | You can't send audio messages in this chat |
| **CHAT_SEND_GAME_FORBIDDEN** | `403` | You can't send a game to this chat |
| **CHAT_SEND_GIFS_FORBIDDEN** | `403` | You can't send gifs in this chat |
| **CHAT_SEND_INLINE_FORBIDDEN** | `403` | You can't send inline messages in this group |
| **CHAT_SEND_MEDIA_FORBIDDEN** | `403` | You can't send media in this chat |
| **CHAT_SEND_PHOTOS_FORBIDDEN** | `403` | You can't send photos in this chat |
| **CHAT_SEND_PLAIN_FORBIDDEN** | `403` | You can't send non-media (text) messages in this chat |
| **CHAT_SEND_STICKERS_FORBIDDEN** | `403` | You can't send stickers in this chat |
| **CHAT_SEND_VOICES_FORBIDDEN** | `403` | You can't send voice recordings in this chat |
| **CHAT_WRITE_FORBIDDEN** | `403` | You can't write in this chat |
| **ENTITY_BOUNDS_INVALID** | `400` | A specified entity offset or length is invalid, see here » for info on how to properly compute the entity offset/length |
| **INLINE_RESULT_EXPIRED** | `400` | The inline query expired |
| **INPUT_USER_DEACTIVATED** | `400` | The specified user was deleted |
| **MEDIA_EMPTY** | `400` | The provided media object is invalid |
| **MSG_ID_INVALID** | `400` | Invalid message ID provided |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |
| **QUERY_ID_EMPTY** | `400` | The query ID is empty |
| **QUICK_REPLIES_TOO_MUCH** | `400` | A maximum of appConfig.quick_replies_limit shortcuts may be created, the limit was reached |
| **RANDOM_ID_DUPLICATE** | `500` | You provided a random ID that was already used |
| **REPLY_MESSAGES_TOO_MUCH** | `400` | Each shortcut can contain a maximum of appConfig.quick_reply_messages_limit messages, the limit was reached |
| **RESULT_ID_EMPTY** | `400` | Result ID empty |
| **RESULT_ID_INVALID** | `400` | One of the specified result IDs is invalid |
| **SCHEDULE_DATE_TOO_LATE** | `400` | You can't schedule a message this far in the future |
| **SCHEDULE_TOO_MUCH** | `400` | There are too many scheduled messages |
| **SEND_MEDIA_INVALID** | `500` | The specified media is invalid |
| **SLOWMODE_WAIT_%d** | `420` | Slowmode is enabled in this chat: wait %d seconds before sending another message to this chat |
| **TOPIC_DELETED** | `400` | The specified topic was deleted |
| **USER_BANNED_IN_CHANNEL** | `400` | You're banned from sending messages in supergroups/channels |
| **VOICE_MESSAGES_FORBIDDEN** | `400` | This user's privacy settings forbid you from sending voice messages |
| **WEBPAGE_CURL_FAILED** | `400` | Failure while fetching the webpage with cURL |
| **WEBPAGE_MEDIA_EMPTY** | `400` | Webpage media empty |
| **YOU_BLOCKED_USER** | `400` | You blocked this user |

---

## Example

```php
$updates = $client->messages->sendInlineBotResult(
	silent : true,
	background : true,
	clear_draft : true,
	hide_via : true,
	peer : $client->inputPeerEmpty(),
	reply_to : $client->inputReplyToMessage(
		reply_to_msg_id : 18,
		top_msg_id : 15,
		reply_to_peer_id : $client->inputPeerEmpty(),
		quote_text : 'rEbJiX0m7qdtpPl3',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 0,
				length : 56,
			),
			$client->messageEntityMention(
				offset : 100,
				length : 23,
			),
			$client->messageEntityHashtag(
				offset : 90,
				length : 33,
			),
			$client->messageEntityBotCommand(
				offset : 10,
				length : 6,
			),
			$client->messageEntityUrl(
				offset : 54,
				length : 90,
			),
			$client->messageEntityEmail(
				offset : 99,
				length : 37,
			),
			$client->messageEntityBold(
				offset : 33,
				length : 66,
			),
			$client->messageEntityItalic(
				offset : 88,
				length : 23,
			),
			$client->messageEntityCode(
				offset : 75,
				length : 25,
			),
			$client->messageEntityPre(
				offset : 61,
				length : 93,
				language : 'uMAfw9j74t1Ox0pe',
			),
			$client->messageEntityTextUrl(
				offset : 83,
				length : 78,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 58,
				length : 85,
				user_id : -3718613804896238524,
			),
			$client->inputMessageEntityMentionName(
				offset : 22,
				length : 88,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 56,
				length : 45,
			),
			$client->messageEntityCashtag(
				offset : 94,
				length : 11,
			),
			$client->messageEntityUnderline(
				offset : 77,
				length : 45,
			),
			$client->messageEntityStrike(
				offset : 24,
				length : 49,
			),
			$client->messageEntityBankCard(
				offset : 79,
				length : 44,
			),
			$client->messageEntitySpoiler(
				offset : 45,
				length : 81,
			),
			$client->messageEntityCustomEmoji(
				offset : 41,
				length : 20,
				document_id : -855287267104009167,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 9,
				length : 9,
			),
		),
		quote_offset : 15,
		monoforum_peer_id : $client->inputPeerEmpty(),
		todo_item_id : 52,
	),
	random_id : -3741107570962950080,
	query_id : 7578147362109795197,
	id : 'wsWGfUFiu6bv9nLg',
	schedule_date : 5,
	send_as : $client->inputPeerEmpty(),
	quick_reply_shortcut : $client->inputQuickReplyShortcut(
		shortcut : '4nU8Cwh7RI0QtfoG',
	),
	allow_paid_stars : 1070584854585822467,
);
```