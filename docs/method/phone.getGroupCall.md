# phone.getGroupCall

**Description** : *Get info about a group call*

**Layer** : 211

```tl
phone.getGroupCall#41845db call:InputGroupCall limit:int = phone.GroupCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>call</mark> | [`InputGroupCall`](type/InputGroupCall) | The group call |
| <mark>limit</mark> | [`int`](type/int) | Maximum number of results to return, see pagination |

---

## Result

[phone.GroupCall](type/phone.GroupCall)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **GROUPCALL_FORBIDDEN** | `403` | The group call has already ended |
| **GROUPCALL_INVALID** | `400` | The specified group call is invalid |

---

## Example

```php
$phoneGroupCall = $client->phone->getGroupCall(
	call : $client->inputGroupCall(
		id : 7023576684239587450,
		access_hash : -7786413731458680283,
	),
	limit : 60,
);
```