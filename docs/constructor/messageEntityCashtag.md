# messageEntityCashtag

**Description** : *Message entity representing a $cashtag*

**Layer** : 211

```tl
messageEntityCashtag#4c4e743f offset:int length:int = MessageEntity;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>offset</mark> | [`int`](type/int) | Offset of message entity within message (in UTF-16 code units) |
| <mark>length</mark> | [`int`](type/int) | Length of message entity within message (in UTF-16 code units) |

---

## Type

[MessageEntity](type/MessageEntity)

---

## Example

```php
$messageEntity = $client->messageEntityCashtag(
	offset : 26,
	length : 2,
);
```