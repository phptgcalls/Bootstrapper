# mediaAreaCoordinates

**Description** : *Coordinates and size of a clicable rectangular area on top of a story*

**Layer** : 211

```tl
mediaAreaCoordinates#cfc9e002 flags:# x:double y:double w:double h:double rotation:double radius:flags.0?double = MediaAreaCoordinates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>x</mark> | [`double`](type/double) | The abscissa of the rectangle's center, as a percentage of the media width (0-100) |
| <mark>y</mark> | [`double`](type/double) | The ordinate of the rectangle's center, as a percentage of the media height (0-100) |
| <mark>w</mark> | [`double`](type/double) | The width of the rectangle, as a percentage of the media width (0-100) |
| <mark>h</mark> | [`double`](type/double) | The height of the rectangle, as a percentage of the media height (0-100) |
| <mark>rotation</mark> | [`double`](type/double) | Clockwise rotation angle of the rectangle, in degrees (0-360) |
| **radius** | [`flags.0?double`](type/double) | The radius of the rectangle corner rounding, as a percentage of the media width |

---

## Type

[MediaAreaCoordinates](type/MediaAreaCoordinates)

---

## Example

```php
$mediaAreaCoordinates = $client->mediaAreaCoordinates(
	x : 341926.490234375,
	y : -382762.9814453125,
	w : -590265.0224609375,
	h : 392397.2314453125,
	rotation : 1268844.7421875,
	radius : -1769874.4521484375,
);
```