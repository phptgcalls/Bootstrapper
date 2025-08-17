# inputFileBig

**Description** : *Assigns a big file (over 10 MB in size), saved in part using the method upload.saveBigFilePart*

**Layer** : 211

```tl
inputFileBig#fa4f0bb5 id:long parts:int name:string = InputFile;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Random file id, created by the client |
| <mark>parts</mark> | [`int`](type/int) | Number of parts saved |
| <mark>name</mark> | [`string`](type/string) | Full file name |

---

## Type

[InputFile](type/InputFile)

---

## Example

```php
$inputFile = $client->inputFileBig(
	id : -8170873106219896458,
	parts : 54,
	name : 'EoSglMs5Kz3kUr0b',
);
```