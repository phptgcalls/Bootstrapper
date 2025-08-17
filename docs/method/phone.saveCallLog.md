# phone.saveCallLog

**Description** : *Save phone call debug information*

**Layer** : 211

```tl
phone.saveCallLog#41248786 peer:InputPhoneCall file:InputFile = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPhoneCall`](type/InputPhoneCall) | Phone call |
| <mark>file</mark> | [`InputFile`](type/InputFile) | Logs |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CALL_PEER_INVALID** | `400` | The provided call peer object is invalid |

---

## Example

```php
$bool = $client->phone->saveCallLog(
	peer : $client->inputPhoneCall(
		id : 2200278248788916703,
		access_hash : 1274785104047357901,
	),
	file : $client->inputFile(
		id : 3546341860951033072,
		parts : 40,
		name : 'xdfojFQ8eSWquEvh',
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
	),
);
```