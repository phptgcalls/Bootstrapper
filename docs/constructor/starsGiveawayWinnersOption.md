# starsGiveawayWinnersOption

**Description** : *Allowed options for the number of giveaway winners*

**Layer** : 211

```tl
starsGiveawayWinnersOption#54236209 flags:# default:flags.0?true users:int per_user_stars:long = StarsGiveawayWinnersOption;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **default** | [`flags.0?true`](type/true) | If set, this option must be pre-selected by default in the option list |
| <mark>users</mark> | [`int`](type/int) | The number of users that will be randomly chosen as winners |
| <mark>per_user_stars</mark> | [`long`](type/long) | The number of Telegram Stars each winner will receive |

---

## Type

[StarsGiveawayWinnersOption](type/StarsGiveawayWinnersOption)

---

## Example

```php
$starsGiveawayWinnersOption = $client->starsGiveawayWinnersOption(
	default : true,
	users : 6,
	per_user_stars : -881439275209272818,
);
```