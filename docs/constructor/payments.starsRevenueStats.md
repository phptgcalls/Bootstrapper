# payments.starsRevenueStats

**Description** : *Star revenue statistics, see here » for more info*

**Layer** : 211

```tl
payments.starsRevenueStats#6c207376 flags:# top_hours_graph:flags.0?StatsGraph revenue_graph:StatsGraph status:StarsRevenueStatus usd_rate:double = payments.StarsRevenueStats;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **top_hours_graph** | [`flags.0?StatsGraph`](type/StatsGraph) | NOTHING |
| <mark>revenue_graph</mark> | [`StatsGraph`](type/StatsGraph) | Star revenue graph (number of earned stars) |
| <mark>status</mark> | [`StarsRevenueStatus`](type/StarsRevenueStatus) | Current balance, current withdrawable balance and overall earned Telegram Stars |
| <mark>usd_rate</mark> | [`double`](type/double) | Current conversion rate of Telegram Stars to USD |

---

## Type

[payments.StarsRevenueStats](type/payments.StarsRevenueStats)

---

## Example

```php
$paymentsStarsRevenueStats = $client->payments->starsRevenueStats(
	top_hours_graph : $client->statsGraphAsync(
		token : 'tbwksUByeroPVgOm',
	),
	revenue_graph : $client->statsGraphAsync(
		token : 'dHS8uvwaP2qcN9gk',
	),
	status : $client->starsRevenueStatus(
		withdrawal_enabled : true,
		current_balance : $client->starsAmount(
			amount : -6541261183376926174,
			nanos : 6,
		),
		available_balance : $client->starsAmount(
			amount : 4073382014565070830,
			nanos : 31,
		),
		overall_revenue : $client->starsAmount(
			amount : 3290747330437789572,
			nanos : 69,
		),
		next_withdrawal_at : 84,
	),
	usd_rate : 455839.1005859375,
);
```