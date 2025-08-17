# channelAdminLogEventActionEditMessage

**Description** : *A message was edited*

**Layer** : 211

```tl
channelAdminLogEventActionEditMessage#709b2405 prev_message:Message new_message:Message = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>prev_message</mark> | [`Message`](type/Message) | Old message |
| <mark>new_message</mark> | [`Message`](type/Message) | New message |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionEditMessage(
	prev_message : $client->messageEmpty(
		id : 25,
		peer_id : $client->peerUser(
			user_id : -7092144303763904984,
		),
	),
	new_message : $client->messageEmpty(
		id : 9,
		peer_id : $client->peerUser(
			user_id : -8688316835313322516,
		),
	),
);
```