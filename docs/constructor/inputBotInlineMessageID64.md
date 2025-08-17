# inputBotInlineMessageID64

**Description** : *Represents a sent inline message from the perspective of a bot*

**Layer** : 211

```tl
inputBotInlineMessageID64#b6d915d7 dc_id:int owner_id:long id:int access_hash:long = InputBotInlineMessageID;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>dc_id</mark> | [`int`](type/int) | DC ID to use when working with this inline message |
| <mark>owner_id</mark> | [`long`](type/long) | ID of the owner of this message |
| <mark>id</mark> | [`int`](type/int) | ID of message |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash of message |

---

## Type

[InputBotInlineMessageID](type/InputBotInlineMessageID)

---

## Example

```php
$inputBotInlineMessageID = $client->inputBotInlineMessageID64(
	dc_id : 13,
	owner_id : -7147057621763689390,
	id : 83,
	access_hash : -809426702643841661,
);
```