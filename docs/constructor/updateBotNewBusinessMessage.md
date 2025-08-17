# updateBotNewBusinessMessage

**Description** : *A message was received via a connected business chat »*

**Layer** : 211

```tl
updateBotNewBusinessMessage#9ddb347c flags:# connection_id:string message:Message reply_to_message:flags.0?Message qts:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>connection_id</mark> | [`string`](type/string) | Connection ID |
| <mark>message</mark> | [`Message`](type/Message) | New message |
| **reply_to_message** | [`flags.0?Message`](type/Message) | The message that message is replying to |
| <mark>qts</mark> | [`int`](type/int) | New qts value, see updates » for more info |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotNewBusinessMessage(
	connection_id : 'uRbB7Y12NryevPHO',
	message : $client->messageEmpty(
		id : 33,
		peer_id : $client->peerUser(
			user_id : 7614205954193046942,
		),
	),
	reply_to_message : $client->messageEmpty(
		id : 85,
		peer_id : $client->peerUser(
			user_id : -6541281491325949216,
		),
	),
	qts : 29,
);
```