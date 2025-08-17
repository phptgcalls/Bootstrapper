# updateChatUserTyping

**Description** : *The user is preparing a message in a group; typing, recording, uploading, etc. This update is valid for 6 seconds. If no further updates of this kind are received after 6 seconds, it should be considered that the user stopped doing whatever they were doing*

**Layer** : 211

```tl
updateChatUserTyping#83487af0 chat_id:long from_id:Peer action:SendMessageAction = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chat_id</mark> | [`long`](type/long) | Group id |
| <mark>from_id</mark> | [`Peer`](type/Peer) | Peer that started typing (can be the chat itself, in case of anonymous admins) |
| <mark>action</mark> | [`SendMessageAction`](type/SendMessageAction) | Type of action |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateChatUserTyping(
	chat_id : 5207858278192382018,
	from_id : $client->peerUser(
		user_id : -8663606042042439133,
	),
	action : $client->sendMessageTypingAction(),
);
```