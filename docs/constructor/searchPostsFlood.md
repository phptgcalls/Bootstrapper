# searchPostsFlood

**Layer** : 211

```tl
searchPostsFlood#3e0b5b6a flags:# query_is_free:flags.0?true total_daily:int remains:int wait_till:flags.1?int stars_amount:long = SearchPostsFlood;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **query_is_free** | [`flags.0?true`](type/true) | NOTHING |
| <mark>total_daily</mark> | [`int`](type/int) | NOTHING |
| <mark>remains</mark> | [`int`](type/int) | NOTHING |
| **wait_till** | [`flags.1?int`](type/int) | NOTHING |
| <mark>stars_amount</mark> | [`long`](type/long) | NOTHING |

---

## Type

[SearchPostsFlood](type/SearchPostsFlood)

---

## Example

```php
$searchPostsFlood = $client->searchPostsFlood(
	query_is_free : true,
	total_daily : 52,
	remains : 17,
	wait_till : 22,
	stars_amount : 8258529066965665850,
);
```