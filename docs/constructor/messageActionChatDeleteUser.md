# messageActionChatDeleteUser

**Description** : *User left the group*

**Layer** : 211

```tl
messageActionChatDeleteUser#a43f30cc user_id:long = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>user_id</mark> | [`long`](type/long) | Leaving user ID |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionChatDeleteUser(
	user_id : -4115272925277022312,
);
```