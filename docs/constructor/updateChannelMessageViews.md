# updateChannelMessageViews

**Description** : *The view counter of a message in a channel has changed*

**Layer** : 211

```tl
updateChannelMessageViews#f226ac08 channel_id:long id:int views:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>channel_id</mark> | [`long`](type/long) | Channel ID |
| <mark>id</mark> | [`int`](type/int) | ID of the message |
| <mark>views</mark> | [`int`](type/int) | New view counter |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateChannelMessageViews(
	channel_id : -5304338690506180016,
	id : 38,
	views : 7,
);
```