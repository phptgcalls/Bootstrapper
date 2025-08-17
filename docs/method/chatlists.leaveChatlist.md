# chatlists.leaveChatlist

**Description** : *Delete a folder imported using a chat folder deep link »*

**Layer** : 211

```tl
chatlists.leaveChatlist#74fae13a chatlist:InputChatlist peers:Vector<InputPeer> = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chatlist</mark> | [`InputChatlist`](type/InputChatlist) | Folder ID |
| <mark>peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | Also leave the specified channels and groups |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **FILTER_ID_INVALID** | `400` | The specified filter ID is invalid |

---

## Example

```php
$updates = $client->chatlists->leaveChatlist(
	chatlist : $client->inputChatlistDialogFilter(
		filter_id : 29,
	),
	peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : -3408107738803954973,
		),
		$client->inputPeerUser(
			user_id : -4738926150864099056,
			access_hash : -8736613724523258320,
		),
		$client->inputPeerChannel(
			channel_id : 3452720295107337730,
			access_hash : 296746769434809436,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 80,
			user_id : 6197481651260420097,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 75,
			channel_id : 6666371355555023355,
		),
	),
);
```