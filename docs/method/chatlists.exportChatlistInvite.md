# chatlists.exportChatlistInvite

**Description** : *Export a folder », creating a chat folder deep link »*

**Layer** : 211

```tl
chatlists.exportChatlistInvite#8472478e chatlist:InputChatlist title:string peers:Vector<InputPeer> = chatlists.ExportedChatlistInvite;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chatlist</mark> | [`InputChatlist`](type/InputChatlist) | The folder to export |
| <mark>title</mark> | [`string`](type/string) | An optional name for the link |
| <mark>peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | The list of channels, group and supergroups to share with the link. Basic groups will automatically be converted to supergroups when invoking the method |

---

## Result

[chatlists.ExportedChatlistInvite](type/chatlists.ExportedChatlistInvite)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHANNEL_INVALID** | `400` | The provided channel is invalid |
| **CHANNEL_PRIVATE** | `400` | You haven't joined this channel/supergroup |
| **CHATLISTS_TOO_MUCH** | `400` | You have created too many folder links, hitting the chatlist_invites_limit_default/chatlist_invites_limit_premium limits » |
| **CHAT_ADMIN_REQUIRED** | `400` | You must be an admin in this chat to do this |
| **FILTER_ID_INVALID** | `400` | The specified filter ID is invalid |
| **FILTER_NOT_SUPPORTED** | `400` | The specified filter cannot be used in this context |
| **INVITES_TOO_MUCH** | `400` | The maximum number of per-folder invites specified by the chatlist_invites_limit_default/chatlist_invites_limit_premium client configuration parameters » was reached |
| **PEERS_LIST_EMPTY** | `400` | The specified list of peers is empty |

---

## Example

```php
$chatlistsExportedChatlistInvite = $client->chatlists->exportChatlistInvite(
	chatlist : $client->inputChatlistDialogFilter(
		filter_id : 24,
	),
	title : 'L0TYlv4KXJ7uqFBG',
	peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : -2925932975300405004,
		),
		$client->inputPeerUser(
			user_id : -3057308332647464493,
			access_hash : -8089956430237086045,
		),
		$client->inputPeerChannel(
			channel_id : -7258088234565062507,
			access_hash : -6005414065815803170,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 8,
			user_id : -3011353768791028406,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 23,
			channel_id : 1280175122668100385,
		),
	),
);
```