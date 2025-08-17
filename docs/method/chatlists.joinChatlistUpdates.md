# chatlists.joinChatlistUpdates

**Description** : *Join channels and supergroups recently added to a chat folder deep link »*

**Layer** : 211

```tl
chatlists.joinChatlistUpdates#e089f8f5 chatlist:InputChatlist peers:Vector<InputPeer> = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chatlist</mark> | [`InputChatlist`](type/InputChatlist) | The folder |
| <mark>peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | List of new chats to join, fetched using chatlists.getChatlistUpdates and filtered as specified in the documentation » |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **FILTER_ID_INVALID** | `400` | The specified filter ID is invalid |
| **FILTER_INCLUDE_EMPTY** | `400` | The include_peers vector of the filter is empty |

---

## Example

```php
$updates = $client->chatlists->joinChatlistUpdates(
	chatlist : $client->inputChatlistDialogFilter(
		filter_id : 33,
	),
	peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : -452677875476684561,
		),
		$client->inputPeerUser(
			user_id : 4355873280753277744,
			access_hash : 3229227159690353792,
		),
		$client->inputPeerChannel(
			channel_id : 4310135579705871844,
			access_hash : -1151515788007708762,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 30,
			user_id : -2545218177110068006,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 81,
			channel_id : -8954461339121220016,
		),
	),
);
```