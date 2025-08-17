# starGiftAttributeModel

**Layer** : 211

```tl
starGiftAttributeModel#39d99013 name:string document:Document rarity_permille:int = StarGiftAttribute;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>name</mark> | [`string`](type/string) | NOTHING |
| <mark>document</mark> | [`Document`](type/Document) | NOTHING |
| <mark>rarity_permille</mark> | [`int`](type/int) | NOTHING |

---

## Type

[StarGiftAttribute](type/StarGiftAttribute)

---

## Example

```php
$starGiftAttribute = $client->starGiftAttributeModel(
	name : 'ar23plO7bcM5VQnu',
	document : $client->documentEmpty(
		id : 3476850901359603280,
	),
	rarity_permille : 70,
);
```