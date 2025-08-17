# mediaAreaChannelPost

**Description** : *Represents a channel post*

**Layer** : 211

```tl
mediaAreaChannelPost#770416af coordinates:MediaAreaCoordinates channel_id:long msg_id:int = MediaArea;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>coordinates</mark> | [`MediaAreaCoordinates`](type/MediaAreaCoordinates) | The size and location of the media area corresponding to the location sticker on top of the story media |
| <mark>channel_id</mark> | [`long`](type/long) | The channel that posted the message |
| <mark>msg_id</mark> | [`int`](type/int) | ID of the channel message |

---

## Type

[MediaArea](type/MediaArea)

---

## Example

```php
$mediaArea = $client->mediaAreaChannelPost(
	coordinates : $client->mediaAreaCoordinates(
		x : 1421434.9658203125,
		y : 1417179.556640625,
		w : 1245053.0419921875,
		h : -352567.1748046875,
		rotation : 794454.548828125,
		radius : 1575289.3779296875,
	),
	channel_id : -8305385913870183522,
	msg_id : 25,
);
```