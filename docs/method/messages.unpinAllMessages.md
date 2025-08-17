# messages.unpinAllMessages

**Description** : *Unpin all pinned messages*

**Layer** : 211

```tl
messages.unpinAllMessages#62dd747 flags:# peer:InputPeer top_msg_id:flags.0?int saved_peer_id:flags.1?InputPeer = messages.AffectedHistory;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Chat where to unpin |
| **top_msg_id** | [`flags.0?int`](type/int) | Forum topic where to unpin |
| **saved_peer_id** | [`flags.1?InputPeer`](type/InputPeer) | NOTHING |

---

## Result

[messages.AffectedHistory](type/messages.AffectedHistory)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHAT_ADMIN_REQUIRED** | `400` | You must be an admin in this chat to do this |
| **CHAT_NOT_MODIFIED** | `400` | No changes were made to chat information because the new information you passed is identical to the current information |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$messagesAffectedHistory = $client->messages->unpinAllMessages(
	peer : $client->inputPeerEmpty(),
	top_msg_id : 90,
	saved_peer_id : $client->inputPeerEmpty(),
);
```