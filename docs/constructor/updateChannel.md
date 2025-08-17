# updateChannel

**Description** : *Channel/supergroup (channel and/or channelFull) information was updated*

**Layer** : 211

```tl
updateChannel#635b4c09 channel_id:long = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>channel_id</mark> | [`long`](type/long) | Channel ID |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateChannel(
	channel_id : -5135851391580117305,
);
```