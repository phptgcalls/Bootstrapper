# messages.affectedHistory

**Description** : *Affected part of communication history with the user or in a chat*

**Layer** : 211

```tl
messages.affectedHistory#b45c69d1 pts:int pts_count:int offset:int = messages.AffectedHistory;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>pts</mark> | [`int`](type/int) | Number of events occurred in a text box |
| <mark>pts_count</mark> | [`int`](type/int) | Number of affected events |
| <mark>offset</mark> | [`int`](type/int) | If a parameter contains positive value, it is necessary to repeat the method call using the given value; during the proceeding of all the history the value itself shall gradually decrease |

---

## Type

[messages.AffectedHistory](type/messages.AffectedHistory)

---

## Example

```php
$messagesAffectedHistory = $client->messages->affectedHistory(
	pts : 89,
	pts_count : 30,
	offset : 23,
);
```