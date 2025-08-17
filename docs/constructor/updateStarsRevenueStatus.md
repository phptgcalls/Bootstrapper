# updateStarsRevenueStatus

**Description** : *The Telegram Star balance of a channel/bot we own has changed »*

**Layer** : 211

```tl
updateStarsRevenueStatus#a584b019 peer:Peer status:StarsRevenueStatus = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | Channel/bot |
| <mark>status</mark> | [`StarsRevenueStatus`](type/StarsRevenueStatus) | New Telegram Star balance |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateStarsRevenueStatus(
	peer : $client->peerUser(
		user_id : -1208168266099801219,
	),
	status : $client->starsRevenueStatus(
		withdrawal_enabled : true,
		current_balance : $client->starsAmount(
			amount : -6216547041808267255,
			nanos : 59,
		),
		available_balance : $client->starsAmount(
			amount : -7184326574725855854,
			nanos : 40,
		),
		overall_revenue : $client->starsAmount(
			amount : -2472147167918543960,
			nanos : 30,
		),
		next_withdrawal_at : 45,
	),
);
```