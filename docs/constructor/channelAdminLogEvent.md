# channelAdminLogEvent

**Description** : *Admin log event*

**Layer** : 211

```tl
channelAdminLogEvent#1fad68cd id:long date:int user_id:long action:ChannelAdminLogEventAction = ChannelAdminLogEvent;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Event ID |
| <mark>date</mark> | [`int`](type/int) | Date |
| <mark>user_id</mark> | [`long`](type/long) | User ID |
| <mark>action</mark> | [`ChannelAdminLogEventAction`](type/ChannelAdminLogEventAction) | Action |

---

## Type

[ChannelAdminLogEvent](type/ChannelAdminLogEvent)

---

## Example

```php
$channelAdminLogEvent = $client->channelAdminLogEvent(
	id : 7826761049022528605,
	date : 66,
	user_id : 3434749031214332045,
	action : $client->channelAdminLogEventActionChangeTitle(
		prev_value : 'uaBWobKxQFPcwH08',
		new_value : 'W9UfIkwi5dOsh6vm',
	),
);
```