# upload.webFile

**Description** : *Represents a chunk of an HTTP webfile downloaded through telegram's secure MTProto servers*

**Layer** : 211

```tl
upload.webFile#21e753bc size:int mime_type:string file_type:storage.FileType mtime:int bytes:bytes = upload.WebFile;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>size</mark> | [`int`](type/int) | File size |
| <mark>mime_type</mark> | [`string`](type/string) | Mime type |
| <mark>file_type</mark> | [`storage.FileType`](type/storage.FileType) | File type |
| <mark>mtime</mark> | [`int`](type/int) | Modified time |
| <mark>bytes</mark> | [`bytes`](type/bytes) | Data |

---

## Type

[upload.WebFile](type/upload.WebFile)

---

## Example

```php
$uploadWebFile = $client->upload->webFile(
	size : 14,
	mime_type : 'rNXE0M6i29al5WH4',
	file_type : $client->storage->fileUnknown(),
	mtime : 89,
	bytes : '?{??4LiveProto6??j?',
);
```