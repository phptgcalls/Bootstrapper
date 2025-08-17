# updateNewMessage

**Description** : *New message in a private chat or in a basic group*

**Layer** : 211

```tl
updateNewMessage#1f2b0afd message:Message pts:int pts_count:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>message</mark> | [`Message`](type/Message) | Message |
| <mark>pts</mark> | [`int`](type/int) | New quantity of actions in a message box |
| <mark>pts_count</mark> | [`int`](type/int) | Number of generated events |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateNewMessage(
	message : $client->messageEmpty(
		id : 79,
		peer_id : $client->peerUser(
			user_id : -8590980322617882485,
		),
	),
	pts : 15,
	pts_count : 95,
);
```