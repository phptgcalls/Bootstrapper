# updateDeleteChannelMessages

**Description** : *Some messages in a supergroup/channel were deleted*

**Layer** : 211

```tl
updateDeleteChannelMessages#c32d5b12 channel_id:long messages:Vector<int> pts:int pts_count:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>channel_id</mark> | [`long`](type/long) | Channel ID |
| <mark>messages</mark> | [`Vector<int>`](type/int) | IDs of messages that were deleted |
| <mark>pts</mark> | [`int`](type/int) | Event count after generation |
| <mark>pts_count</mark> | [`int`](type/int) | Number of events that were generated |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateDeleteChannelMessages(
	channel_id : 4955042302496368556,
	messages : array(7),
	pts : 4,
	pts_count : 56,
);
```