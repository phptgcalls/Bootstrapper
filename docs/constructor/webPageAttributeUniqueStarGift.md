# webPageAttributeUniqueStarGift

**Layer** : 211

```tl
webPageAttributeUniqueStarGift#cf6f6db8 gift:StarGift = WebPageAttribute;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>gift</mark> | [`StarGift`](type/StarGift) | NOTHING |

---

## Type

[WebPageAttribute](type/WebPageAttribute)

---

## Example

```php
$webPageAttribute = $client->webPageAttributeUniqueStarGift(
	gift : $client->starGift(
		limited : true,
		sold_out : true,
		birthday : true,
		require_premium : true,
		limited_per_user : true,
		id : 5296429538382570375,
		sticker : $client->documentEmpty(
			id : 5778949763586589794,
		),
		stars : -3518271820261044883,
		availability_remains : 68,
		availability_total : 55,
		availability_resale : 1196687538316523225,
		convert_stars : 6457764068401179482,
		first_sale_date : 25,
		last_sale_date : 79,
		upgrade_stars : -551498714471973513,
		resell_min_stars : 3295525584381988163,
		title : 'COVdj0Ix1P5tJ7AL',
		released_by : $client->peerUser(
			user_id : -8576814192740918368,
		),
		per_user_total : 69,
		per_user_remains : 88,
	),
);
```