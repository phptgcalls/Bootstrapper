# updateReadHistoryOutbox

**Description** : *Outgoing messages were read*

**Layer** : 211

```tl
updateReadHistoryOutbox#2f2f21bf peer:Peer max_id:int pts:int pts_count:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | Peer |
| <mark>max_id</mark> | [`int`](type/int) | Maximum ID of read outgoing messages |
| <mark>pts</mark> | [`int`](type/int) | Event count after generation |
| <mark>pts_count</mark> | [`int`](type/int) | Number of events that were generated |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateReadHistoryOutbox(
	peer : $client->peerUser(
		user_id : 7012230984652352339,
	),
	max_id : 85,
	pts : 88,
	pts_count : 50,
);
```