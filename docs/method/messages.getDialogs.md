# messages.getDialogs

**Description** : *Returns the current user dialog list*

**Layer** : 211

```tl
messages.getDialogs#a0f4cb4f flags:# exclude_pinned:flags.0?true folder_id:flags.1?int offset_date:int offset_id:int offset_peer:InputPeer limit:int hash:long = messages.Dialogs;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **exclude_pinned** | [`flags.0?true`](type/true) | Exclude pinned dialogs |
| **folder_id** | [`flags.1?int`](type/int) | Peer folder ID, for more info click here |
| <mark>offset_date</mark> | [`int`](type/int) | Offsets for pagination, for more info click here |
| <mark>offset_id</mark> | [`int`](type/int) | Offsets for pagination, for more info click here (top_message ID used for pagination) |
| <mark>offset_peer</mark> | [`InputPeer`](type/InputPeer) | Offset peer for pagination |
| <mark>limit</mark> | [`int`](type/int) | Number of list elements to be returned |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Result

[messages.Dialogs](type/messages.Dialogs)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHAT_WRITE_FORBIDDEN** | `403` | You can't write in this chat |
| **FOLDER_ID_INVALID** | `400` | Invalid folder ID |
| **OFFSET_PEER_ID_INVALID** | `400` | The provided offset peer is invalid |
| **TAKEOUT_INVALID** | `400` | The specified takeout ID is invalid |

---

## Example

```php
$messagesDialogs = $client->messages->getDialogs(
	exclude_pinned : true,
	folder_id : 73,
	offset_date : 98,
	offset_id : 37,
	offset_peer : $client->inputPeerEmpty(),
	limit : 1,
	hash : 5549058968072009685,
);
```