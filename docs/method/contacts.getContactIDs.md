# contacts.getContactIDs

**Description** : *Get the telegram IDs of all contacts.
Returns an array of Telegram user IDs for all contacts (0 if a contact does not have an associated Telegram account or have hidden their account using privacy settings)*

**Layer** : 211

```tl
contacts.getContactIDs#7adc669d hash:long = Vector<int>;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Result

[Vector<int>](type/int)

---

## Example

```php
$int = $client->contacts->getContactIDs(
	hash : 1204710913272149946,
);
```