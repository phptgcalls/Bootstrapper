# pageListOrderedItemText

**Description** : *Ordered list of text items*

**Layer** : 211

```tl
pageListOrderedItemText#5e068047 num:string text:RichText = PageListOrderedItem;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>num</mark> | [`string`](type/string) | Number of element within ordered list |
| <mark>text</mark> | [`RichText`](type/RichText) | Text |

---

## Type

[PageListOrderedItem](type/PageListOrderedItem)

---

## Example

```php
$pageListOrderedItem = $client->pageListOrderedItemText(
	num : 'tYE3yLU7grabiAIm',
	text : $client->textEmpty(),
);
```