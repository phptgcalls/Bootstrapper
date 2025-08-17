# photoCachedSize

**Description** : *Description of an image and its content*

**Layer** : 211

```tl
photoCachedSize#21e1ad6 type:string w:int h:int bytes:bytes = PhotoSize;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>type</mark> | [`string`](type/string) | Thumbnail type |
| <mark>w</mark> | [`int`](type/int) | Image width |
| <mark>h</mark> | [`int`](type/int) | Image height |
| <mark>bytes</mark> | [`bytes`](type/bytes) | Binary data, file content |

---

## Type

[PhotoSize](type/PhotoSize)

---

## Example

```php
$photoSize = $client->photoCachedSize(
	type : 'yVdcmZ8GCp27J4UQ',
	w : 16,
	h : 62,
	bytes : '?pny*LiveProto?K?6?',
);
```