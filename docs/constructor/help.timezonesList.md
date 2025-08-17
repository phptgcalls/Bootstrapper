# help.timezonesList

**Description** : *Timezone information that may be used elsewhere in the API, such as to set Telegram Business opening hours »*

**Layer** : 211

```tl
help.timezonesList#7b74ed71 timezones:Vector<Timezone> hash:int = help.TimezonesList;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>timezones</mark> | [`Vector<Timezone>`](type/Timezone) | Timezones |
| <mark>hash</mark> | [`int`](type/int) | Hash used for caching, for more info click here |

---

## Type

[help.TimezonesList](type/help.TimezonesList)

---

## Example

```php
$helpTimezonesList = $client->help->timezonesList(
	timezones : array(
		$client->timezone(
			id : 'Ho61dtY2cFRyDaqE',
			name : 'LGU7sHrDSZucQmJb',
			utc_offset : 40,
		),
	),
	hash : 12,
);
```