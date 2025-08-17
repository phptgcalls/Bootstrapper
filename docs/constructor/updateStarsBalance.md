# updateStarsBalance

**Description** : *The current account's Telegram Stars balance » has changed*

**Layer** : 211

```tl
updateStarsBalance#4e80a379 balance:StarsAmount = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>balance</mark> | [`StarsAmount`](type/StarsAmount) | New balance |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateStarsBalance(
	balance : $client->starsAmount(
		amount : 8586995705856470574,
		nanos : 73,
	),
);
```