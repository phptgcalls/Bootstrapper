# inputDocument

**Description** : *Defines a document for subsequent interaction*

**Layer** : 211

```tl
inputDocument#1abfb575 id:long access_hash:long file_reference:bytes = InputDocument;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Document ID |
| <mark>access_hash</mark> | [`long`](type/long) | access_hash parameter from the document constructor |
| <mark>file_reference</mark> | [`bytes`](type/bytes) | File reference |

---

## Type

[InputDocument](type/InputDocument)

---

## Example

```php
$inputDocument = $client->inputDocument(
	id : 7390388372200220182,
	access_hash : 6871182124416259328,
	file_reference : ',??LiveProto6?ie?',
);
```