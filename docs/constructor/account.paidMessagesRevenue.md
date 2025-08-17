# account.paidMessagesRevenue

**Layer** : 211

```tl
account.paidMessagesRevenue#1e109708 stars_amount:long = account.PaidMessagesRevenue;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>stars_amount</mark> | [`long`](type/long) | NOTHING |

---

## Type

[account.PaidMessagesRevenue](type/account.PaidMessagesRevenue)

---

## Example

```php
$accountPaidMessagesRevenue = $client->account->paidMessagesRevenue(
	stars_amount : -3098867330191825808,
);
```