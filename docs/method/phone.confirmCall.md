# phone.confirmCall

**Description** : *Complete phone call E2E encryption key exchange »*

**Layer** : 211

```tl
phone.confirmCall#2efe1722 peer:InputPhoneCall g_a:bytes key_fingerprint:long protocol:PhoneCallProtocol = phone.PhoneCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPhoneCall`](type/InputPhoneCall) | The phone call |
| <mark>g_a</mark> | [`bytes`](type/bytes) | Parameter for E2E encryption key exchange » |
| <mark>key_fingerprint</mark> | [`long`](type/long) | Key fingerprint |
| <mark>protocol</mark> | [`PhoneCallProtocol`](type/PhoneCallProtocol) | Phone call settings |

---

## Result

[phone.PhoneCall](type/phone.PhoneCall)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CALL_ALREADY_DECLINED** | `400` | The call was already declined |
| **CALL_PEER_INVALID** | `400` | The provided call peer object is invalid |

---

## Example

```php
$phonePhoneCall = $client->phone->confirmCall(
	peer : $client->inputPhoneCall(
		id : 7186151816115906361,
		access_hash : -8346613729308048451,
	),
	g_a : '?X|??LiveProtow?~?Q',
	key_fingerprint : 5131533041076832784,
	protocol : $client->phoneCallProtocol(
		udp_p2p : true,
		udp_reflector : true,
		min_layer : 50,
		max_layer : 57,
		library_versions : array('V57FOUixe3PdEfoZ'),
	),
);
```