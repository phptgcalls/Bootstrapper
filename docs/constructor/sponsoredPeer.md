# sponsoredPeer

**Layer** : 211

```tl
sponsoredPeer#c69708d3 flags:# random_id:bytes peer:Peer sponsor_info:flags.0?string additional_info:flags.1?string = SponsoredPeer;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| <mark>random_id</mark> | [`bytes`](type/bytes) | NOTHING |
| <mark>peer</mark> | [`Peer`](type/Peer) | NOTHING |
| **sponsor_info** | [`flags.0?string`](type/string) | NOTHING |
| **additional_info** | [`flags.1?string`](type/string) | NOTHING |

---

## Type

[SponsoredPeer](type/SponsoredPeer)

---

## Example

```php
$sponsoredPeer = $client->sponsoredPeer(
	random_id : '?"?7?LiveProto?e?H?',
	peer : $client->peerUser(
		user_id : 6861726888289267126,
	),
	sponsor_info : 'E52gN6YhyRGp7L3t',
	additional_info : 'aej0Zz4nWdOmkrh5',
);
```