# inputPhotoFileLocation

**Description** : *Use this object to download a photo with upload.getFile method*

**Layer** : 211

```tl
inputPhotoFileLocation#40181ffe id:long access_hash:long file_reference:bytes thumb_size:string = InputFileLocation;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Photo ID, obtained from the photo object |
| <mark>access_hash</mark> | [`long`](type/long) | Photo's access hash, obtained from the photo object |
| <mark>file_reference</mark> | [`bytes`](type/bytes) | File reference |
| <mark>thumb_size</mark> | [`string`](type/string) | The PhotoSize to download: must be set to the type field of the desired PhotoSize object of the photo |

---

## Type

[InputFileLocation](type/InputFileLocation)

---

## Example

```php
$inputFileLocation = $client->inputPhotoFileLocation(
	id : -6359291254629636016,
	access_hash : 7218597939857584702,
	file_reference : 'y_$??LiveProto??vE',
	thumb_size : 'Nn3JRCT45hey1LtU',
);
```