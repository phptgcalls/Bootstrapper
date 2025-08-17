# inputPeerUser

**Description** : *Defines a user for further interaction*

**Layer** : 211

```tl
inputPeerUser#dde8a54c user_id:long access_hash:long = InputPeer;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>user_id</mark> | [`long`](type/long) | User identifier |
| <mark>access_hash</mark> | [`long`](type/long) | access_hash value from the user constructor |

---

## Type

[InputPeer](type/InputPeer)

---

## Example

```php
$inputPeer = $client->inputPeerUser(
	user_id : 8396506714798546855,
	access_hash : 7280082277225642834,
);
```