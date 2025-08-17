# messages.affectedMessages

**Description** : *Events affected by operation*

**Layer** : 211

```tl
messages.affectedMessages#84d19185 pts:int pts_count:int = messages.AffectedMessages;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>pts</mark> | [`int`](type/int) | Event count after generation |
| <mark>pts_count</mark> | [`int`](type/int) | Number of events that were generated |

---

## Type

[messages.AffectedMessages](type/messages.AffectedMessages)

---

## Example

```php
$messagesAffectedMessages = $client->messages->affectedMessages(
	pts : 35,
	pts_count : 37,
);
```