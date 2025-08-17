# channelAdminLogEventActionDeleteMessage

**Description** : *A message was deleted*

**Layer** : 211

```tl
channelAdminLogEventActionDeleteMessage#42e047bb message:Message = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>message</mark> | [`Message`](type/Message) | The message that was deleted |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionDeleteMessage(
	message : $client->messageEmpty(
		id : 46,
		peer_id : $client->peerUser(
			user_id : -6362913294107271602,
		),
	),
);
```