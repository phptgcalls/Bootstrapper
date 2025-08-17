# updateBusinessBotCallbackQuery

**Description** : *A callback button sent via a business connection was pressed, and the button data was sent to the bot that created the button*

**Layer** : 211

```tl
updateBusinessBotCallbackQuery#1ea2fda7 flags:# query_id:long user_id:long connection_id:string message:Message reply_to_message:flags.2?Message chat_instance:long data:flags.0?bytes = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>query_id</mark> | [`long`](type/long) | Query ID |
| <mark>user_id</mark> | [`long`](type/long) | ID of the user that pressed the button |
| <mark>connection_id</mark> | [`string`](type/string) | Business connection ID |
| <mark>message</mark> | [`Message`](type/Message) | Message that contains the keyboard (also contains info about the chat where the message was sent) |
| **reply_to_message** | [`flags.2?Message`](type/Message) | The message that message is replying to |
| <mark>chat_instance</mark> | [`long`](type/long) | Global identifier, uniquely corresponding to the chat to which the message with the callback button was sent. Useful for high scores in games |
| **data** | [`flags.0?bytes`](type/bytes) | Callback data |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBusinessBotCallbackQuery(
	query_id : 7510166196581312133,
	user_id : -1540742262910779899,
	connection_id : 'QGW9m08Do24qnRYj',
	message : $client->messageEmpty(
		id : 80,
		peer_id : $client->peerUser(
			user_id : 1298037463981261386,
		),
	),
	reply_to_message : $client->messageEmpty(
		id : 66,
		peer_id : $client->peerUser(
			user_id : 5422889804566339622,
		),
	),
	chat_instance : 5388739050078486637,
	data : '??X*3LiveProto??',
);
```