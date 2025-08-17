# inputBusinessIntro

**Description** : *Telegram Business introduction »*

**Layer** : 211

```tl
inputBusinessIntro#9c469cd flags:# title:string description:string sticker:flags.0?InputDocument = InputBusinessIntro;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>title</mark> | [`string`](type/string) | Title of the introduction message |
| <mark>description</mark> | [`string`](type/string) | Profile introduction |
| **sticker** | [`flags.0?InputDocument`](type/InputDocument) | Optional introduction sticker |

---

## Type

[InputBusinessIntro](type/InputBusinessIntro)

---

## Example

```php
$inputBusinessIntro = $client->inputBusinessIntro(
	title : 'viOb1AxSVZqUXj62',
	description : '8UD3XcAgonSTZmPs',
	sticker : $client->inputDocumentEmpty(),
);
```