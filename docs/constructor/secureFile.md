# secureFile

**Description** : *Secure passport file, for more info see the passport docs »*

**Layer** : 211

```tl
secureFile#7d09c27e id:long access_hash:long size:long dc_id:int date:int file_hash:bytes secret:bytes = SecureFile;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | ID |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash |
| <mark>size</mark> | [`long`](type/long) | File size |
| <mark>dc_id</mark> | [`int`](type/int) | DC ID |
| <mark>date</mark> | [`int`](type/int) | Date of upload |
| <mark>file_hash</mark> | [`bytes`](type/bytes) | File hash |
| <mark>secret</mark> | [`bytes`](type/bytes) | Secret |

---

## Type

[SecureFile](type/SecureFile)

---

## Example

```php
$secureFile = $client->secureFile(
	id : 9175747384529412813,
	access_hash : 6137293450558420451,
	size : -7720949510137248822,
	dc_id : 92,
	date : 48,
	file_hash : 'o-?YLiveProtoNL?',
	secret : 'k)0?0LiveProto?
??',
);
```