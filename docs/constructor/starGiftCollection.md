# starGiftCollection

**Layer** : 211

```tl
starGiftCollection#9d6b13b0 flags:# collection_id:int title:string icon:flags.0?Document gifts_count:int hash:long = StarGiftCollection;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| <mark>collection_id</mark> | [`int`](type/int) | NOTHING |
| <mark>title</mark> | [`string`](type/string) | NOTHING |
| **icon** | [`flags.0?Document`](type/Document) | NOTHING |
| <mark>gifts_count</mark> | [`int`](type/int) | NOTHING |
| <mark>hash</mark> | [`long`](type/long) | NOTHING |

---

## Type

[StarGiftCollection](type/StarGiftCollection)

---

## Example

```php
$starGiftCollection = $client->starGiftCollection(
	collection_id : 90,
	title : 'DzdIwq5OT3lxn2Lg',
	icon : $client->documentEmpty(
		id : 2443380779706016524,
	),
	gifts_count : 57,
	hash : -1602498314566819609,
);
```