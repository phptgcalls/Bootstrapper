# messages.readReactions

**Description** : *Mark message reactions » as read*

**Layer** : 211

```tl
messages.readReactions#9ec44f93 flags:# peer:InputPeer top_msg_id:flags.0?int saved_peer_id:flags.1?InputPeer = messages.AffectedHistory;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Peer |
| **top_msg_id** | [`flags.0?int`](type/int) | Mark as read only reactions to messages within the specified forum topic |
| **saved_peer_id** | [`flags.1?InputPeer`](type/InputPeer) | NOTHING |

---

## Result

[messages.AffectedHistory](type/messages.AffectedHistory)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$messagesAffectedHistory = $client->messages->readReactions(
	peer : $client->inputPeerEmpty(),
	top_msg_id : 92,
	saved_peer_id : $client->inputPeerEmpty(),
);
```