# messageActionConferenceCall

**Layer** : 211

```tl
messageActionConferenceCall#2ffe2f7a flags:# missed:flags.0?true active:flags.1?true video:flags.4?true call_id:long duration:flags.2?int other_participants:flags.3?Vector<Peer> = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **missed** | [`flags.0?true`](type/true) | NOTHING |
| **active** | [`flags.1?true`](type/true) | NOTHING |
| **video** | [`flags.4?true`](type/true) | NOTHING |
| <mark>call_id</mark> | [`long`](type/long) | NOTHING |
| **duration** | [`flags.2?int`](type/int) | NOTHING |
| **other_participants** | [`flags.3?Vector<Peer>`](type/Peer) | NOTHING |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionConferenceCall(
	missed : true,
	active : true,
	video : true,
	call_id : -5019074868926487766,
	duration : 61,
	other_participants : array(
		$client->peerUser(
			user_id : 4277298813999263764,
		),
		$client->peerChat(
			chat_id : -6951105940864996319,
		),
		$client->peerChannel(
			channel_id : -6801342533321288615,
		),
	),
);
```