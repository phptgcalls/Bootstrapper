# geoPointAddress

**Description** : *Address optionally associated to a geoPoint*

**Layer** : 211

```tl
geoPointAddress#de4c5d93 flags:# country_iso2:string state:flags.0?string city:flags.1?string street:flags.2?string = GeoPointAddress;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>country_iso2</mark> | [`string`](type/string) | Two-letter ISO 3166-1 alpha-2 country code |
| **state** | [`flags.0?string`](type/string) | State |
| **city** | [`flags.1?string`](type/string) | City |
| **street** | [`flags.2?string`](type/string) | Street |

---

## Type

[GeoPointAddress](type/GeoPointAddress)

---

## Example

```php
$geoPointAddress = $client->geoPointAddress(
	country_iso2 : 'JjdfebNMGFyTU2PC',
	state : '36fdrHBbFSRKj50w',
	city : '4I0pNUmhxMlo7Sbg',
	street : 'Y1Zg8fkhnDXiObcs',
);
```