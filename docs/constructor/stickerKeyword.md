# stickerKeyword

**Description** : *Keywords for a certain sticker*

**Layer** : 211

```tl
stickerKeyword#fcfeb29c document_id:long keyword:Vector<string> = StickerKeyword;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>document_id</mark> | [`long`](type/long) | Sticker ID |
| <mark>keyword</mark> | [`Vector<string>`](type/string) | Keywords |

---

## Type

[StickerKeyword](type/StickerKeyword)

---

## Example

```php
$stickerKeyword = $client->stickerKeyword(
	document_id : 4256391573962728115,
	keyword : array('6DfC5TYJed8p3E74'),
);
```