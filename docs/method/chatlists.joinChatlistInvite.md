# chatlists.joinChatlistInvite

**Description** : *Import a chat folder deep link », joining some or all the chats in the folder*

**Layer** : 211

```tl
chatlists.joinChatlistInvite#a6b1e39a slug:string peers:Vector<InputPeer> = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>slug</mark> | [`string`](type/string) | slug obtained from a chat folder deep link » |
| <mark>peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | List of new chats to join, fetched using chatlists.checkChatlistInvite and filtered as specified in the documentation » |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **FILTER_INCLUDE_EMPTY** | `400` | The include_peers vector of the filter is empty |
| **INVITE_SLUG_EMPTY** | `400` | The specified invite slug is empty |
| **INVITE_SLUG_EXPIRED** | `400` | The specified chat folder link has expired |

---

## Example

```php
$updates = $client->chatlists->joinChatlistInvite(
	slug : 'FEOdtwzxr7hGAyDb',
	peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : -9175578393859119504,
		),
		$client->inputPeerUser(
			user_id : 42141431115500612,
			access_hash : -8441582759808966762,
		),
		$client->inputPeerChannel(
			channel_id : -7504936929337106003,
			access_hash : 196726509644457435,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 56,
			user_id : 6932008803204863681,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 6,
			channel_id : 5853994781903085334,
		),
	),
);
```