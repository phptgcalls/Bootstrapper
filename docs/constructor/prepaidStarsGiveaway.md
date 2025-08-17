# prepaidStarsGiveaway

**Description** : *Contains info about a prepaid Telegram Star giveaway »*

**Layer** : 211

```tl
prepaidStarsGiveaway#9a9d77e0 id:long stars:long quantity:int boosts:int date:int = PrepaidGiveaway;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Prepaid giveaway ID |
| <mark>stars</mark> | [`long`](type/long) | Number of given away Telegram Stars » |
| <mark>quantity</mark> | [`int`](type/int) | Number of giveaway winners |
| <mark>boosts</mark> | [`int`](type/int) | Number of boosts the channel will gain by launching the giveaway |
| <mark>date</mark> | [`int`](type/int) | When was the giveaway paid for |

---

## Type

[PrepaidGiveaway](type/PrepaidGiveaway)

---

## Example

```php
$prepaidGiveaway = $client->prepaidStarsGiveaway(
	id : -6967266180991655079,
	stars : 6228578792358081014,
	quantity : 60,
	boosts : 10,
	date : 9,
);
```