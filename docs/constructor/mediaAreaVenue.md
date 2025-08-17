# mediaAreaVenue

**Description** : *Represents a location tag attached to a story, with additional venue information*

**Layer** : 211

```tl
mediaAreaVenue#be82db9c coordinates:MediaAreaCoordinates geo:GeoPoint title:string address:string provider:string venue_id:string venue_type:string = MediaArea;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>coordinates</mark> | [`MediaAreaCoordinates`](type/MediaAreaCoordinates) | The size and location of the media area corresponding to the location sticker on top of the story media |
| <mark>geo</mark> | [`GeoPoint`](type/GeoPoint) | Coordinates of the venue |
| <mark>title</mark> | [`string`](type/string) | Venue name |
| <mark>address</mark> | [`string`](type/string) | Address |
| <mark>provider</mark> | [`string`](type/string) | Venue provider: currently only "foursquare" needs to be supported |
| <mark>venue_id</mark> | [`string`](type/string) | Venue ID in the provider's database |
| <mark>venue_type</mark> | [`string`](type/string) | Venue type in the provider's database |

---

## Type

[MediaArea](type/MediaArea)

---

## Example

```php
$mediaArea = $client->mediaAreaVenue(
	coordinates : $client->mediaAreaCoordinates(
		x : 2088264.9814453125,
		y : 305718.453125,
		w : 62992.2744140625,
		h : -591458.9443359375,
		rotation : 2016056.2138671875,
		radius : 1358863.646484375,
	),
	geo : $client->geoPointEmpty(),
	title : 'yRhKfTU1dnDMol5a',
	address : 'cJ3Cfpq4ua1DZAQB',
	provider : 'RJmC0AYkr3VL8uyw',
	venue_id : 'lyaeZsAVhgW25PEq',
	venue_type : 'Y9JTFfyxsjp6iKIr',
);
```