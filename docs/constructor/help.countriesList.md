# help.countriesList

**Description** : *Name, ISO code, localized name and phone codes/patterns of all available countries*

**Layer** : 211

```tl
help.countriesList#87d0759e countries:Vector<help.Country> hash:int = help.CountriesList;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>countries</mark> | [`Vector<help.Country>`](type/help.Country) | Name, ISO code, localized name and phone codes/patterns of all available countries |
| <mark>hash</mark> | [`int`](type/int) | Hash used for caching, for more info click here |

---

## Type

[help.CountriesList](type/help.CountriesList)

---

## Example

```php
$helpCountriesList = $client->help->countriesList(
	countries : array(
		$client->help->country(
			hidden : true,
			iso2 : 'YGpT0nZedaAUurgC',
			default_name : 'cEz2Z5xNstwOhGDR',
			name : 'dUxi4CRAw60Jgp19',
			country_codes : array(
				$client->help->countryCode(
					country_code : 'dmoZtwFWOKEfYChb',
					prefixes : array('o1hPp2YRjqHaDrk5'),
					patterns : array('e7LD4mE8bFn5yB1O'),
				),
			),
		),
	),
	hash : 45,
);
```