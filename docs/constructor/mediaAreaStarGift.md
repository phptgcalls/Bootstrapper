# mediaAreaStarGift

**Layer** : 211

```tl
mediaAreaStarGift#5787686d coordinates:MediaAreaCoordinates slug:string = MediaArea;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>coordinates</mark> | [`MediaAreaCoordinates`](type/MediaAreaCoordinates) | NOTHING |
| <mark>slug</mark> | [`string`](type/string) | NOTHING |

---

## Type

[MediaArea](type/MediaArea)

---

## Example

```php
$mediaArea = $client->mediaAreaStarGift(
	coordinates : $client->mediaAreaCoordinates(
		x : -811539.6787109375,
		y : 1512727.0244140625,
		w : -296478.1845703125,
		h : 1178000.990234375,
		rotation : 1978409.306640625,
		radius : 1750629.771484375,
	),
	slug : 'lpndzwru4Wsg8GME',
);
```