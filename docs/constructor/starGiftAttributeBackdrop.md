# starGiftAttributeBackdrop

**Layer** : 211

```tl
starGiftAttributeBackdrop#d93d859c name:string backdrop_id:int center_color:int edge_color:int pattern_color:int text_color:int rarity_permille:int = StarGiftAttribute;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>name</mark> | [`string`](type/string) | NOTHING |
| <mark>backdrop_id</mark> | [`int`](type/int) | NOTHING |
| <mark>center_color</mark> | [`int`](type/int) | NOTHING |
| <mark>edge_color</mark> | [`int`](type/int) | NOTHING |
| <mark>pattern_color</mark> | [`int`](type/int) | NOTHING |
| <mark>text_color</mark> | [`int`](type/int) | NOTHING |
| <mark>rarity_permille</mark> | [`int`](type/int) | NOTHING |

---

## Type

[StarGiftAttribute](type/StarGiftAttribute)

---

## Example

```php
$starGiftAttribute = $client->starGiftAttributeBackdrop(
	name : 'ZixD7MQoVba2pFBE',
	backdrop_id : 40,
	center_color : 21,
	edge_color : 12,
	pattern_color : 58,
	text_color : 18,
	rarity_permille : 53,
);
```