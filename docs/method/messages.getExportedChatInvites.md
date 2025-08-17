# messages.getExportedChatInvites

**Description** : *Get info about the chat invites of a specific chat*

**Layer** : 211

```tl
messages.getExportedChatInvites#a2b5a3f6 flags:# revoked:flags.3?true peer:InputPeer admin_id:InputUser offset_date:flags.2?int offset_link:flags.2?string limit:int = messages.ExportedChatInvites;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **revoked** | [`flags.3?true`](type/true) | Whether to fetch revoked chat invites |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Chat |
| <mark>admin_id</mark> | [`InputUser`](type/InputUser) | Whether to only fetch chat invites from this admin |
| **offset_date** | [`flags.2?int`](type/int) | Offsets for pagination, for more info click here |
| **offset_link** | [`flags.2?string`](type/string) | Offsets for pagination, for more info click here |
| <mark>limit</mark> | [`int`](type/int) | Maximum number of results to return, see pagination |

---

## Result

[messages.ExportedChatInvites](type/messages.ExportedChatInvites)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **ADMIN_ID_INVALID** | `400` | The specified admin ID is invalid |
| **CHANNEL_INVALID** | `400` | The provided channel is invalid |
| **CHANNEL_PRIVATE** | `400` | You haven't joined this channel/supergroup |
| **CHAT_ADMIN_REQUIRED** | `400` | You must be an admin in this chat to do this |
| **CHAT_WRITE_FORBIDDEN** | `403` | You can't write in this chat |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$messagesExportedChatInvites = $client->messages->getExportedChatInvites(
	revoked : true,
	peer : $client->inputPeerEmpty(),
	admin_id : $client->inputUserEmpty(),
	offset_date : 81,
	offset_link : 'Z5sBxmtSbMy3qoTW',
	limit : 49,
);
```