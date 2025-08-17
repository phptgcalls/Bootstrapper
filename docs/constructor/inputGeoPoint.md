# inputGeoPoint

**Description** : *Defines a GeoPoint by its coordinates*

**Layer** : 211

```tl
inputGeoPoint#48222faf flags:# lat:double long:double accuracy_radius:flags.0?int = InputGeoPoint;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>lat</mark> | [`double`](type/double) | Latitude |
| <mark>long</mark> | [`double`](type/double) | Longitude |
| **accuracy_radius** | [`flags.0?int`](type/int) | The estimated horizontal accuracy of the location, in meters; as defined by the sender |

---

## Type

[InputGeoPoint](type/InputGeoPoint)

---

## Example

```php
$inputGeoPoint = $client->inputGeoPoint(
	lat : -1283703.6396484375,
	long : -1889402.8193359375,
	accuracy_radius : 58,
);
```