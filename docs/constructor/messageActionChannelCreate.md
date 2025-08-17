# messageActionChannelCreate

**Description** : *The channel was created*

**Layer** : 211

```tl
messageActionChannelCreate#95d2ac92 title:string = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>title</mark> | [`string`](type/string) | Original channel/supergroup title |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionChannelCreate(
	title : 'KH2GAqQx7JOhpig1',
);
```