# statsDateRangeDays

**Description** : *Channel statistics date range*

**Layer** : 211

```tl
statsDateRangeDays#b637edaf min_date:int max_date:int = StatsDateRangeDays;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>min_date</mark> | [`int`](type/int) | Initial date |
| <mark>max_date</mark> | [`int`](type/int) | Final date |

---

## Type

[StatsDateRangeDays](type/StatsDateRangeDays)

---

## Example

```php
$statsDateRangeDays = $client->statsDateRangeDays(
	min_date : 12,
	max_date : 65,
);
```