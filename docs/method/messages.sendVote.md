# messages.sendVote

**Description** : *Vote in a poll*

**Layer** : 211

```tl
messages.sendVote#10ea6184 peer:InputPeer msg_id:int options:Vector<bytes> = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | The chat where the poll was sent |
| <mark>msg_id</mark> | [`int`](type/int) | The message ID of the poll |
| <mark>options</mark> | [`Vector<bytes>`](type/bytes) | The options that were chosen |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHANNEL_INVALID** | `400` | The provided channel is invalid |
| **CHANNEL_PRIVATE** | `400` | You haven't joined this channel/supergroup |
| **MESSAGE_ID_INVALID** | `400` | The provided message id is invalid |
| **MESSAGE_POLL_CLOSED** | `400` | Poll closed |
| **MSG_ID_INVALID** | `400` | Invalid message ID provided |
| **OPTIONS_TOO_MUCH** | `400` | Too many options provided |
| **OPTION_INVALID** | `400` | Invalid option selected |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |
| **REVOTE_NOT_ALLOWED** | `400` | You cannot change your vote |

---

## Example

```php
$updates = $client->messages->sendVote(
	peer : $client->inputPeerEmpty(),
	msg_id : 17,
	options : array('?5t?-LiveProtoK??Z!'),
);
```