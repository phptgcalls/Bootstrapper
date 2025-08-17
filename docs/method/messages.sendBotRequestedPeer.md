# messages.sendBotRequestedPeer

**Description** : *Send one or more chosen peers, as requested by a keyboardButtonRequestPeer button*

**Layer** : 211

```tl
messages.sendBotRequestedPeer#91b2d060 peer:InputPeer msg_id:int button_id:int requested_peers:Vector<InputPeer> = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | The bot that sent the keyboardButtonRequestPeer button |
| <mark>msg_id</mark> | [`int`](type/int) | ID of the message that contained the reply keyboard with the keyboardButtonRequestPeer button |
| <mark>button_id</mark> | [`int`](type/int) | The button_id field from the keyboardButtonRequestPeer constructor |
| <mark>requested_peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | The chosen peers |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **MESSAGE_ID_INVALID** | `400` | The provided message id is invalid |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$updates = $client->messages->sendBotRequestedPeer(
	peer : $client->inputPeerEmpty(),
	msg_id : 98,
	button_id : 27,
	requested_peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : -7844739003845203389,
		),
		$client->inputPeerUser(
			user_id : -4998468949622915284,
			access_hash : -7482607872339948827,
		),
		$client->inputPeerChannel(
			channel_id : -920525090579133069,
			access_hash : 7776583822967269621,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 66,
			user_id : -5015774583031669264,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 75,
			channel_id : 6908554103202722281,
		),
	),
);
```