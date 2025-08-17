# upload.getFileHashes

**Description** : *Get SHA256 hashes for verifying downloaded files*

**Layer** : 211

```tl
upload.getFileHashes#9156982a location:InputFileLocation offset:long = Vector<FileHash>;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>location</mark> | [`InputFileLocation`](type/InputFileLocation) | File |
| <mark>offset</mark> | [`long`](type/long) | Offset from which to get file hashes |

---

## Result

[Vector<FileHash>](type/FileHash)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **LOCATION_INVALID** | `400` | The provided location is invalid |

---

## Example

```php
$fileHash = $client->upload->getFileHashes(
	location : $client->inputFileLocation(
		volume_id : 5318302245908775090,
		local_id : 92,
		secret : -2151640388544951318,
		file_reference : 'yQe?3LiveProto???Z',
	),
	offset : 9162344914387019940,
);
```