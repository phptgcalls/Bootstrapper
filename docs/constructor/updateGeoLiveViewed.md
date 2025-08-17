# updateGeoLiveViewed

**Description** : *Live geoposition message was viewed*

**Layer** : 211

```tl
updateGeoLiveViewed#871fb939 peer:Peer msg_id:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | The user that viewed the live geoposition |
| <mark>msg_id</mark> | [`int`](type/int) | Message ID of geoposition message |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateGeoLiveViewed(
	peer : $client->peerUser(
		user_id : -2896400092387429953,
	),
	msg_id : 86,
);
```