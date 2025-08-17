# phone.createConferenceCall

**Layer** : 211

```tl
phone.createConferenceCall#7d0444bb flags:# muted:flags.0?true video_stopped:flags.2?true join:flags.3?true random_id:int public_key:flags.3?int256 block:flags.3?bytes params:flags.3?DataJSON = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **muted** | [`flags.0?true`](type/true) | NOTHING |
| **video_stopped** | [`flags.2?true`](type/true) | NOTHING |
| **join** | [`flags.3?true`](type/true) | NOTHING |
| <mark>random_id</mark> | [`int`](type/int) | NOTHING |
| **public_key** | [`flags.3?int256`](type/int256) | NOTHING |
| **block** | [`flags.3?bytes`](type/bytes) | NOTHING |
| **params** | [`flags.3?DataJSON`](type/DataJSON) | NOTHING |

---

## Result

[Updates](type/Updates)

---

## Example

```php
$updates = $client->phone->createConferenceCall(
	muted : true,
	video_stopped : true,
	join : true,
	random_id : 84,
	public_key : '105839463295528119604373766712616397086723300137789220494780763398420133007654',
	block : 'Y?u?LiveProto' . "\0" . '??B?',
	params : $client->dataJSON(
		data : '48qpaZ6hzFKQXLxl',
	),
);
```