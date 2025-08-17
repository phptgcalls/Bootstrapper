# inputMediaUploadedPhoto

**Description** : *Photo*

**Layer** : 211

```tl
inputMediaUploadedPhoto#1e287d04 flags:# spoiler:flags.2?true file:InputFile stickers:flags.0?Vector<InputDocument> ttl_seconds:flags.1?int = InputMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **spoiler** | [`flags.2?true`](type/true) | Whether this media should be hidden behind a spoiler warning |
| <mark>file</mark> | [`InputFile`](type/InputFile) | The uploaded file |
| **stickers** | [`flags.0?Vector<InputDocument>`](type/InputDocument) | Attached mask stickers |
| **ttl_seconds** | [`flags.1?int`](type/int) | Time to live in seconds of self-destructing photo |

---

## Type

[InputMedia](type/InputMedia)

---

## Example

```php
$inputMedia = $client->inputMediaUploadedPhoto(
	spoiler : true,
	file : $client->inputFile(
		id : -8853180215139682752,
		parts : 70,
		name : '8brZ3l5hgtXBuUd4',
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
	),
	stickers : array(
		$client->inputDocumentEmpty(),
		$client->inputDocument(
			id : -3429300624086752779,
			access_hash : 4486894404891173496,
			file_reference : '??F8?LiveProtoS	?',
		),
	),
	ttl_seconds : 99,
);
```