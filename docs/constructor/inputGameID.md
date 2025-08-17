# inputGameID

**Description** : *Indicates an already sent game*

**Layer** : 211

```tl
inputGameID#32c3e77 id:long access_hash:long = InputGame;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | game ID from Game constructor |
| <mark>access_hash</mark> | [`long`](type/long) | access hash from Game constructor |

---

## Type

[InputGame](type/InputGame)

---

## Example

```php
$inputGame = $client->inputGameID(
	id : 2935837390764535812,
	access_hash : -1381244020920218593,
);
```