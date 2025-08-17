# messageActionRequestedPeer

**Description** : *Contains info about one or more peers that the we (the user) shared with the bot after clicking on a keyboardButtonRequestPeer button (service message sent by the user)*

**Layer** : 211

```tl
messageActionRequestedPeer#31518e9b button_id:int peers:Vector<Peer> = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>button_id</mark> | [`int`](type/int) | button_id contained in the keyboardButtonRequestPeer |
| <mark>peers</mark> | [`Vector<Peer>`](type/Peer) | The shared peers |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionRequestedPeer(
	button_id : 27,
	peers : array(
		$client->peerUser(
			user_id : -5165463801999347626,
		),
		$client->peerChat(
			chat_id : -6493212620286743239,
		),
		$client->peerChannel(
			channel_id : -8573200452972191790,
		),
	),
);
```