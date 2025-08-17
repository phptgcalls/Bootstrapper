# phoneCallAccepted

**Description** : *An accepted phone call*

**Layer** : 211

```tl
phoneCallAccepted#3660c311 flags:# video:flags.6?true id:long access_hash:long date:int admin_id:long participant_id:long g_b:bytes protocol:PhoneCallProtocol = PhoneCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **video** | [`flags.6?true`](type/true) | Whether this is a video call |
| <mark>id</mark> | [`long`](type/long) | ID of accepted phone call |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash of phone call |
| <mark>date</mark> | [`int`](type/int) | When was the call accepted |
| <mark>admin_id</mark> | [`long`](type/long) | ID of the call creator |
| <mark>participant_id</mark> | [`long`](type/long) | ID of the other user in the call |
| <mark>g_b</mark> | [`bytes`](type/bytes) | B parameter for secure E2E phone call key exchange |
| <mark>protocol</mark> | [`PhoneCallProtocol`](type/PhoneCallProtocol) | Protocol to use for phone call |

---

## Type

[PhoneCall](type/PhoneCall)

---

## Example

```php
$phoneCall = $client->phoneCallAccepted(
	video : true,
	id : -3229093451233204700,
	access_hash : -1708809390844001872,
	date : 89,
	admin_id : -353997808495891875,
	participant_id : 1548135117047232882,
	g_b : '?]	{bLiveProto??:',
	protocol : $client->phoneCallProtocol(
		udp_p2p : true,
		udp_reflector : true,
		min_layer : 93,
		max_layer : 80,
		library_versions : array('E9GJ5bkWMLAh8dtn'),
	),
);
```