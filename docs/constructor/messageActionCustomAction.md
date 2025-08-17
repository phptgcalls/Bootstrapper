# messageActionCustomAction

**Description** : *Custom action (most likely not supported by the current layer, an upgrade might be needed)*

**Layer** : 211

```tl
messageActionCustomAction#fae69f56 message:string = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>message</mark> | [`string`](type/string) | Action message |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionCustomAction(
	message : '9fUeNAYEgvO5HDtk',
);
```