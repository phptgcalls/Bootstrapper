# upload.saveBigFilePart

**Description** : *Saves a part of a large file (over 10 MB in size) to be later passed to one of the methods*

**Layer** : 211

```tl
upload.saveBigFilePart#de7b673d file_id:long file_part:int file_total_parts:int bytes:bytes = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>file_id</mark> | [`long`](type/long) | Random file id, created by the client |
| <mark>file_part</mark> | [`int`](type/int) | Part sequence number |
| <mark>file_total_parts</mark> | [`int`](type/int) | Total number of parts |
| <mark>bytes</mark> | [`bytes`](type/bytes) | Binary data, part contents |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **FILE_PARTS_INVALID** | `400` | The number of file parts is invalid |
| **FILE_PART_EMPTY** | `400` | The provided file part is empty |
| **FILE_PART_INVALID** | `400` | The file part number is invalid |
| **FILE_PART_SIZE_CHANGED** | `400` | Provided file part size has changed |
| **FILE_PART_SIZE_INVALID** | `400` | The provided file part size is invalid |
| **FILE_PART_TOO_BIG** | `400` | The uploaded file part is too big |
| **FILE_PART_TOO_SMALL** | `400` | The size of the uploaded file part is too small, please see the documentation for the allowed sizes |

---

## Example

```php
$bool = $client->upload->saveBigFilePart(
	file_id : -1065076582454174865,
	file_part : 15,
	file_total_parts : 9,
	bytes : '4ܫ?LiveProto?^.??',
);
```