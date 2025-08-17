# messages.getSavedDialogsByID

**Layer** : 211

```tl
messages.getSavedDialogsByID#6f6f9c96 flags:# parent_peer:flags.1?InputPeer ids:Vector<InputPeer> = messages.SavedDialogs;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **parent_peer** | [`flags.1?InputPeer`](type/InputPeer) | NOTHING |
| <mark>ids</mark> | [`Vector<InputPeer>`](type/InputPeer) | NOTHING |

---

## Result

[messages.SavedDialogs](type/messages.SavedDialogs)

---

## Example

```php
$messagesSavedDialogs = $client->messages->getSavedDialogsByID(
	parent_peer : $client->inputPeerEmpty(),
	ids : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : 5619126420477038201,
		),
		$client->inputPeerUser(
			user_id : -1945672191182701010,
			access_hash : -3591398895578934613,
		),
		$client->inputPeerChannel(
			channel_id : 4724158910397577582,
			access_hash : 1325655867364571977,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 36,
			user_id : 719477159541756347,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 73,
			channel_id : -2110724499548284836,
		),
	),
);
```