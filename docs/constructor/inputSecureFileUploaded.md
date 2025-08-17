# inputSecureFileUploaded

**Description** : *Uploaded secure file, for more info see the passport docs »*

**Layer** : 211

```tl
inputSecureFileUploaded#3334b0f0 id:long parts:int md5_checksum:string file_hash:bytes secret:bytes = InputSecureFile;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Secure file ID |
| <mark>parts</mark> | [`int`](type/int) | Secure file part count |
| <mark>md5_checksum</mark> | [`string`](type/string) | MD5 hash of encrypted uploaded file, to be checked server-side |
| <mark>file_hash</mark> | [`bytes`](type/bytes) | File hash |
| <mark>secret</mark> | [`bytes`](type/bytes) | Secret |

---

## Type

[InputSecureFile](type/InputSecureFile)

---

## Example

```php
$inputSecureFile = $client->inputSecureFileUploaded(
	id : 7887308256866252423,
	parts : 54,
	md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
	file_hash : '2GP?LiveProto?Z???',
	secret : '?w??LiveProto????',
);
```