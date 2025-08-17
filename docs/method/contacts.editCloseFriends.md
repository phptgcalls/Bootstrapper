# contacts.editCloseFriends

**Description** : *Edit the close friends list, see here » for more info*

**Layer** : 211

```tl
contacts.editCloseFriends#ba6705f0 id:Vector<long> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`Vector<long>`](type/long) | Full list of user IDs of close friends, see here for more info |

---

## Result

[Bool](type/Bool)

---

## Example

```php
$bool = $client->contacts->editCloseFriends(
	id : array(-777953109695968658),
);
```