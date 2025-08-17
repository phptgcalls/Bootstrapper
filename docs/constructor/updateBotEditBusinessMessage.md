# updateBotEditBusinessMessage

**Description** : *A message was edited in a connected business chat »*

**Layer** : 211

```tl
updateBotEditBusinessMessage#7df587c flags:# connection_id:string message:Message reply_to_message:flags.0?Message qts:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>connection_id</mark> | [`string`](type/string) | Business connection ID |
| <mark>message</mark> | [`Message`](type/Message) | New message |
| **reply_to_message** | [`flags.0?Message`](type/Message) | The message that message is replying to |
| <mark>qts</mark> | [`int`](type/int) | New qts value, see updates » for more info |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotEditBusinessMessage(
	connection_id : 'V0IdHgvC6M13r4ub',
	message : $client->messageEmpty(
		id : 83,
		peer_id : $client->peerUser(
			user_id : -3816471967503208796,
		),
	),
	reply_to_message : $client->messageEmpty(
		id : 43,
		peer_id : $client->peerUser(
			user_id : -8149866367958407673,
		),
	),
	qts : 71,
);
```