# mediaAreaWeather

**Description** : *Represents a weather widget »*

**Layer** : 211

```tl
mediaAreaWeather#49a6549c coordinates:MediaAreaCoordinates emoji:string temperature_c:double color:int = MediaArea;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>coordinates</mark> | [`MediaAreaCoordinates`](type/MediaAreaCoordinates) | The size and location of the media area corresponding to the widget on top of the story media |
| <mark>emoji</mark> | [`string`](type/string) | Weather emoji, should be rendered as an animated emoji |
| <mark>temperature_c</mark> | [`double`](type/double) | Temperature in degrees Celsius |
| <mark>color</mark> | [`int`](type/int) | ARGB background color |

---

## Type

[MediaArea](type/MediaArea)

---

## Example

```php
$mediaArea = $client->mediaAreaWeather(
	coordinates : $client->mediaAreaCoordinates(
		x : 1454499.5380859375,
		y : 1798318.150390625,
		w : 1525815.7666015625,
		h : 968972.78125,
		rotation : -1797694.2978515625,
		radius : -105553.2265625,
	),
	emoji : 'KA1HOZSJi5qu9B0N',
	temperature_c : 430436.2529296875,
	color : 95,
);
```