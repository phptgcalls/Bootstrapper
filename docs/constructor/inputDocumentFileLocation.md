# inputDocumentFileLocation

**Description** : *Document location (video, voice, audio, basically every type except photo)*

**Layer** : 211

```tl
inputDocumentFileLocation#bad07584 id:long access_hash:long file_reference:bytes thumb_size:string = InputFileLocation;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Document ID |
| <mark>access_hash</mark> | [`long`](type/long) | access_hash parameter from the document constructor |
| <mark>file_reference</mark> | [`bytes`](type/bytes) | File reference |
| <mark>thumb_size</mark> | [`string`](type/string) | Thumbnail size to download the thumbnail |

---

## Type

[InputFileLocation](type/InputFileLocation)

---

## Example

```php
$inputFileLocation = $client->inputDocumentFileLocation(
	id : 3199205366705004944,
	access_hash : -4616106422016012458,
	file_reference : '\\???4LiveProtoeY???',
	thumb_size : 'B6mGhwPYgltKDELj',
);
```