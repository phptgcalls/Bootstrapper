# updateQuickReplyMessage

**Description** : *A new message was added to a quick reply shortcut »*

**Layer** : 211

```tl
updateQuickReplyMessage#3e050d0f message:Message = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>message</mark> | [`Message`](type/Message) | The message that was added (the message.quick_reply_shortcut_id field will contain the shortcut ID) |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateQuickReplyMessage(
	message : $client->messageEmpty(
		id : 48,
		peer_id : $client->peerUser(
			user_id : -4474367902655930244,
		),
	),
);
```