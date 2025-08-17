# phone.deleteConferenceCallParticipants

**Layer** : 211

```tl
phone.deleteConferenceCallParticipants#8ca60525 flags:# only_left:flags.0?true kick:flags.1?true call:InputGroupCall ids:Vector<long> block:bytes = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **only_left** | [`flags.0?true`](type/true) | NOTHING |
| **kick** | [`flags.1?true`](type/true) | NOTHING |
| <mark>call</mark> | [`InputGroupCall`](type/InputGroupCall) | NOTHING |
| <mark>ids</mark> | [`Vector<long>`](type/long) | NOTHING |
| <mark>block</mark> | [`bytes`](type/bytes) | NOTHING |

---

## Result

[Updates](type/Updates)

---

## Example

```php
$updates = $client->phone->deleteConferenceCallParticipants(
	only_left : true,
	kick : true,
	call : $client->inputGroupCall(
		id : -1568827319186641423,
		access_hash : 6851368300284301264,
	),
	ids : array(-2616468204074635465),
	block : 'K?EqLiveProto?F?!' . "\0" . '',
);
```