# phone.discardGroupCall

**Description** : *Terminate a group call*

**Layer** : 211

```tl
phone.discardGroupCall#7a777135 call:InputGroupCall = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>call</mark> | [`InputGroupCall`](type/InputGroupCall) | The group call to terminate |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **GROUPCALL_ALREADY_DISCARDED** | `400` | The group call was already discarded |
| **GROUPCALL_FORBIDDEN** | `403` | The group call has already ended |
| **GROUPCALL_INVALID** | `400` | The specified group call is invalid |

---

## Example

```php
$updates = $client->phone->discardGroupCall(
	call : $client->inputGroupCall(
		id : 4964881355105174730,
		access_hash : 7480878623014531932,
	),
);
```