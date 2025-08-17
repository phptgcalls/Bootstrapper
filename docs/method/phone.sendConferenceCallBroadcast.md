# phone.sendConferenceCallBroadcast

**Layer** : 211

```tl
phone.sendConferenceCallBroadcast#c6701900 call:InputGroupCall block:bytes = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>call</mark> | [`InputGroupCall`](type/InputGroupCall) | NOTHING |
| <mark>block</mark> | [`bytes`](type/bytes) | NOTHING |

---

## Result

[Updates](type/Updates)

---

## Example

```php
$updates = $client->phone->sendConferenceCallBroadcast(
	call : $client->inputGroupCall(
		id : 119049918566596872,
		access_hash : -1150250454113657008,
	),
	block : '?1ԭ?LiveProto?ٟ?]',
);
```