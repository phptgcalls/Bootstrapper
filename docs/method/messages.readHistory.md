# messages.readHistory

**Description** : *Marks message history as read*

**Layer** : 211

```tl
messages.readHistory#e306d3a peer:InputPeer max_id:int = messages.AffectedMessages;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Target user or group |
| <mark>max_id</mark> | [`int`](type/int) | If a positive value is passed, only messages with identifiers less or equal than the given one will be read |

---

## Result

[messages.AffectedMessages](type/messages.AffectedMessages)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHANNEL_PRIVATE** | `400` | You haven't joined this channel/supergroup |
| **CHAT_ID_INVALID** | `400` | The provided chat id is invalid |
| **MSG_ID_INVALID** | `400` | Invalid message ID provided |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$messagesAffectedMessages = $client->messages->readHistory(
	peer : $client->inputPeerEmpty(),
	max_id : 83,
);
```