# todoCompletion

**Layer** : 211

```tl
todoCompletion#4cc120b7 id:int completed_by:long date:int = TodoCompletion;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`int`](type/int) | NOTHING |
| <mark>completed_by</mark> | [`long`](type/long) | NOTHING |
| <mark>date</mark> | [`int`](type/int) | NOTHING |

---

## Type

[TodoCompletion](type/TodoCompletion)

---

## Example

```php
$todoCompletion = $client->todoCompletion(
	id : 13,
	completed_by : 8590532601229109293,
	date : 23,
);
```