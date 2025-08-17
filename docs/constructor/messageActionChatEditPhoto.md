# messageActionChatEditPhoto

**Description** : *Group profile changed*

**Layer** : 211

```tl
messageActionChatEditPhoto#7fcb13a8 photo:Photo = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>photo</mark> | [`Photo`](type/Photo) | New group profile photo |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionChatEditPhoto(
	photo : $client->photoEmpty(
		id : -3356776246713856475,
	),
);
```