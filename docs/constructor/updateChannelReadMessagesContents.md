# updateChannelReadMessagesContents

**Description** : *The specified channel/supergroup messages were read*

**Layer** : 211

```tl
updateChannelReadMessagesContents#25f324f7 flags:# channel_id:long top_msg_id:flags.0?int saved_peer_id:flags.1?Peer messages:Vector<int> = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>channel_id</mark> | [`long`](type/long) | Channel/supergroup ID |
| **top_msg_id** | [`flags.0?int`](type/int) | Forum topic ID |
| **saved_peer_id** | [`flags.1?Peer`](type/Peer) | NOTHING |
| <mark>messages</mark> | [`Vector<int>`](type/int) | IDs of messages that were read |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateChannelReadMessagesContents(
	channel_id : -8608571806323450175,
	top_msg_id : 73,
	saved_peer_id : $client->peerUser(
		user_id : 6810566806274764187,
	),
	messages : array(81),
);
```