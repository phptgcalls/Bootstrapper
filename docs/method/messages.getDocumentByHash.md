# messages.getDocumentByHash

**Description** : *Get a document by its SHA256 hash, mainly used for gifs*

**Layer** : 211

```tl
messages.getDocumentByHash#b1f2061f sha256:bytes size:long mime_type:string = Document;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>sha256</mark> | [`bytes`](type/bytes) | SHA256 of file |
| <mark>size</mark> | [`long`](type/long) | Size of the file in bytes |
| <mark>mime_type</mark> | [`string`](type/string) | Mime type |

---

## Result

[Document](type/Document)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **SHA256_HASH_INVALID** | `400` | The provided SHA256 hash is invalid |

---

## Example

```php
$document = $client->messages->getDocumentByHash(
	sha256 : '?z?LiveProtoa?!??',
	size : 775859180268708199,
	mime_type : 'njdNHL4E3hGbXQWZ',
);
```