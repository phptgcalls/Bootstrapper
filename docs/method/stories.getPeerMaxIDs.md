# stories.getPeerMaxIDs

**Description** : *Get the IDs of the maximum read stories for a set of peers*

**Layer** : 211

```tl
stories.getPeerMaxIDs#535983c3 id:Vector<InputPeer> = Vector<int>;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`Vector<InputPeer>`](type/InputPeer) | Peers |

---

## Result

[Vector<int>](type/int)

---

## Example

```php
$int = $client->stories->getPeerMaxIDs(
	id : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : -7580624876682653215,
		),
		$client->inputPeerUser(
			user_id : -8821725582738446768,
			access_hash : -3405527193575523918,
		),
		$client->inputPeerChannel(
			channel_id : -251036659882087518,
			access_hash : -6444945207801000448,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 75,
			user_id : 7035195182137702189,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 100,
			channel_id : -4264881742649495583,
		),
	),
);
```