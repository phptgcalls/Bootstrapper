# mediaAreaUrl

**Description** : *Represents a URL media area*

**Layer** : 211

```tl
mediaAreaUrl#37381085 coordinates:MediaAreaCoordinates url:string = MediaArea;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>coordinates</mark> | [`MediaAreaCoordinates`](type/MediaAreaCoordinates) | The size and location of the media area corresponding to the URL button on top of the story media |
| <mark>url</mark> | [`string`](type/string) | URL to open when clicked |

---

## Type

[MediaArea](type/MediaArea)

---

## Example

```php
$mediaArea = $client->mediaAreaUrl(
	coordinates : $client->mediaAreaCoordinates(
		x : 385549.4765625,
		y : -611333.3955078125,
		w : 1008122.86328125,
		h : 2022269.021484375,
		rotation : 1575022.93359375,
		radius : 1985109.291015625,
	),
	url : 'https://docs.liveproto.dev',
);
```