# shippingOption

**Description** : *Shipping option*

**Layer** : 211

```tl
shippingOption#b6213cdf id:string title:string prices:Vector<LabeledPrice> = ShippingOption;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`string`](type/string) | Option ID |
| <mark>title</mark> | [`string`](type/string) | Title |
| <mark>prices</mark> | [`Vector<LabeledPrice>`](type/LabeledPrice) | List of price portions |

---

## Type

[ShippingOption](type/ShippingOption)

---

## Example

```php
$shippingOption = $client->shippingOption(
	id : 'r19cfIHAgajnQoBh',
	title : 'OluMPLvH30Soiz7e',
	prices : array(
		$client->labeledPrice(
			label : 'qCBmNHWpvwVjFbtz',
			amount : -8414079785639341016,
		),
	),
);
```