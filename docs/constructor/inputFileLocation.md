# inputFileLocation

**Description** : *DEPRECATED location of a photo*

**Layer** : 211

```tl
inputFileLocation#dfdaabe1 volume_id:long local_id:int secret:long file_reference:bytes = InputFileLocation;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>volume_id</mark> | [`long`](type/long) | Server volume |
| <mark>local_id</mark> | [`int`](type/int) | File identifier |
| <mark>secret</mark> | [`long`](type/long) | Check sum to access the file |
| <mark>file_reference</mark> | [`bytes`](type/bytes) | File reference |

---

## Type

[InputFileLocation](type/InputFileLocation)

---

## Example

```php
$inputFileLocation = $client->inputFileLocation(
	volume_id : -5667203600867862623,
	local_id : 60,
	secret : -2220763364750812950,
	file_reference : '?W?LiveProto???,?',
);
```