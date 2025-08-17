# updatePeerLocated

**Description** : *List of peers near you was updated*

**Layer** : 211

```tl
updatePeerLocated#b4afcfb0 peers:Vector<PeerLocated> = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peers</mark> | [`Vector<PeerLocated>`](type/PeerLocated) | Geolocated peer list update |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updatePeerLocated(
	peers : array(
		$client->peerLocated(
			peer : $client->peerUser(
				user_id : -1219279234856995869,
			),
			expires : 75,
			distance : 24,
		),
		$client->peerSelfLocated(
			expires : 100,
		),
	),
);
```