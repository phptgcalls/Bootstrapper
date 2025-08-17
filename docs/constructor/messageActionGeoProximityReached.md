# messageActionGeoProximityReached

**Description** : *A user of the chat is now in proximity of another user*

**Layer** : 211

```tl
messageActionGeoProximityReached#98e0d697 from_id:Peer to_id:Peer distance:int = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>from_id</mark> | [`Peer`](type/Peer) | The user or chat that is now in proximity of to_id |
| <mark>to_id</mark> | [`Peer`](type/Peer) | The user or chat that subscribed to live geolocation proximity alerts |
| <mark>distance</mark> | [`int`](type/int) | Distance, in meters (0-100000) |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionGeoProximityReached(
	from_id : $client->peerUser(
		user_id : -2368362823748401879,
	),
	to_id : $client->peerUser(
		user_id : 5561386364979310210,
	),
	distance : 29,
);
```