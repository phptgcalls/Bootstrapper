# channelAdminLogEventActionUpdatePinned

**Description** : *A message was pinned*

**Layer** : 211

```tl
channelAdminLogEventActionUpdatePinned#e9e82c18 message:Message = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>message</mark> | [`Message`](type/Message) | The message that was pinned |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionUpdatePinned(
	message : $client->messageEmpty(
		id : 45,
		peer_id : $client->peerUser(
			user_id : -4418136534268490925,
		),
	),
);
```