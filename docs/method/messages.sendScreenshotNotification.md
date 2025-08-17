# messages.sendScreenshotNotification

**Description** : *Notify the other user in a private chat that a screenshot of the chat was taken*

**Layer** : 211

```tl
messages.sendScreenshotNotification#a1405817 peer:InputPeer reply_to:InputReplyTo random_id:long = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Other user |
| <mark>reply_to</mark> | [`InputReplyTo`](type/InputReplyTo) | Indicates the message that was screenshotted (the specified message ID can also be 0 to avoid indicating any specific message) |
| <mark>random_id</mark> | [`long`](type/long) | Random ID to avoid message resending |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **INPUT_USER_DEACTIVATED** | `400` | The specified user was deleted |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |
| **REPLY_MESSAGE_ID_INVALID** | `400` | The specified reply-to message ID is invalid |
| **STORY_ID_INVALID** | `400` | The specified story ID is invalid |
| **YOU_BLOCKED_USER** | `400` | You blocked this user |

---

## Example

```php
$updates = $client->messages->sendScreenshotNotification(
	peer : $client->inputPeerEmpty(),
	reply_to : $client->inputReplyToMessage(
		reply_to_msg_id : 100,
		top_msg_id : 88,
		reply_to_peer_id : $client->inputPeerEmpty(),
		quote_text : 'yVW5oOmharJnbK9S',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 87,
				length : 53,
			),
			$client->messageEntityMention(
				offset : 24,
				length : 69,
			),
			$client->messageEntityHashtag(
				offset : 25,
				length : 42,
			),
			$client->messageEntityBotCommand(
				offset : 35,
				length : 67,
			),
			$client->messageEntityUrl(
				offset : 29,
				length : 35,
			),
			$client->messageEntityEmail(
				offset : 39,
				length : 82,
			),
			$client->messageEntityBold(
				offset : 16,
				length : 99,
			),
			$client->messageEntityItalic(
				offset : 69,
				length : 78,
			),
			$client->messageEntityCode(
				offset : 37,
				length : 53,
			),
			$client->messageEntityPre(
				offset : 63,
				length : 92,
				language : '0J5ZqedyGQ2LTFYo',
			),
			$client->messageEntityTextUrl(
				offset : 32,
				length : 52,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 100,
				length : 66,
				user_id : -7732793308748198023,
			),
			$client->inputMessageEntityMentionName(
				offset : 78,
				length : 20,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 51,
				length : 4,
			),
			$client->messageEntityCashtag(
				offset : 30,
				length : 90,
			),
			$client->messageEntityUnderline(
				offset : 36,
				length : 10,
			),
			$client->messageEntityStrike(
				offset : 2,
				length : 89,
			),
			$client->messageEntityBankCard(
				offset : 13,
				length : 34,
			),
			$client->messageEntitySpoiler(
				offset : 36,
				length : 89,
			),
			$client->messageEntityCustomEmoji(
				offset : 94,
				length : 7,
				document_id : -876290947877306221,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 26,
				length : 25,
			),
		),
		quote_offset : 0,
		monoforum_peer_id : $client->inputPeerEmpty(),
		todo_item_id : 33,
	),
	random_id : -2032185837697645455,
);
```