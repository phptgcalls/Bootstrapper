# phoneCall

**Description** : *Phone call*

**Layer** : 211

```tl
phoneCall#30535af5 flags:# p2p_allowed:flags.5?true video:flags.6?true conference_supported:flags.8?true id:long access_hash:long date:int admin_id:long participant_id:long g_a_or_b:bytes key_fingerprint:long protocol:PhoneCallProtocol connections:Vector<PhoneConnection> start_date:int custom_parameters:flags.7?DataJSON = PhoneCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **p2p_allowed** | [`flags.5?true`](type/true) | Whether P2P connection to the other peer is allowed |
| **video** | [`flags.6?true`](type/true) | Whether this is a video call |
| **conference_supported** | [`flags.8?true`](type/true) | NOTHING |
| <mark>id</mark> | [`long`](type/long) | Call ID |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash |
| <mark>date</mark> | [`int`](type/int) | Date of creation of the call |
| <mark>admin_id</mark> | [`long`](type/long) | User ID of the creator of the call |
| <mark>participant_id</mark> | [`long`](type/long) | User ID of the other participant in the call |
| <mark>g_a_or_b</mark> | [`bytes`](type/bytes) | Parameter for key exchange |
| <mark>key_fingerprint</mark> | [`long`](type/long) | Key fingerprint |
| <mark>protocol</mark> | [`PhoneCallProtocol`](type/PhoneCallProtocol) | Call protocol info to be passed to libtgvoip |
| <mark>connections</mark> | [`Vector<PhoneConnection>`](type/PhoneConnection) | List of endpoints the user can connect to exchange call data |
| <mark>start_date</mark> | [`int`](type/int) | When was the call actually started |
| **custom_parameters** | [`flags.7?DataJSON`](type/DataJSON) | Custom JSON-encoded call parameters to be passed to tgcalls |

---

## Type

[PhoneCall](type/PhoneCall)

---

## Example

```php
$phoneCall = $client->phoneCall(
	p2p_allowed : true,
	video : true,
	conference_supported : true,
	id : -3789351336883562255,
	access_hash : 5985180998065153214,
	date : 47,
	admin_id : -8235081104460700986,
	participant_id : -4209387219227432020,
	g_a_or_b : '^?<YLiveProto?;(?',
	key_fingerprint : -4038940238632972283,
	protocol : $client->phoneCallProtocol(
		udp_p2p : true,
		udp_reflector : true,
		min_layer : 1,
		max_layer : 54,
		library_versions : array('YLDofRz9al6SJIiK'),
	),
	connections : array(
		$client->phoneConnection(
			tcp : true,
			id : -931514042006265222,
			ip : '127.0.0.1',
			ipv6 : '127.0.0.1',
			port : 7,
			peer_tag : '???6?LiveProto????e',
		),
		$client->phoneConnectionWebrtc(
			turn : true,
			stun : true,
			id : -7788197424011788411,
			ip : '127.0.0.1',
			ipv6 : '127.0.0.1',
			port : 0,
			username : 'TakNone',
			password : 'XIbqzNmZST0pa6kU',
		),
	),
	start_date : 57,
	custom_parameters : $client->dataJSON(
		data : '6LV537z8ajwgq0IC',
	),
);
```