# updateLangPack

**Description** : *Language pack updated*

**Layer** : 211

```tl
updateLangPack#56022f4d difference:LangPackDifference = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>difference</mark> | [`LangPackDifference`](type/LangPackDifference) | Changed strings |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateLangPack(
	difference : $client->langPackDifference(
		lang_code : '0N9YwRJ8lGuQVOrv',
		from_version : 45,
		version : 39,
		strings : array(
			$client->langPackString(
				key : 'btgzDV3Gn4iuvpoW',
				value : 'jklHwLSg1nFxrK24',
			),
			$client->langPackStringPluralized(
				key : 'snZl6rY08SypIRcP',
				zero_value : '5lMfuKt7iVowXBUb',
				one_value : 'Vf3ndvRNM8gstwTF',
				two_value : 'KYBaR4bQG2o9HEd3',
				few_value : 'f2EQ18mKnjVhUoSv',
				many_value : 'EWeTaVrPRoMySnm0',
				other_value : 'WHBTegl8Pdixmt9S',
			),
			$client->langPackStringDeleted(
				key : 'psrQ1FCbcKYB8w52',
			),
		),
	),
);
```