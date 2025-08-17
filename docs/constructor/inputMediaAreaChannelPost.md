# inputMediaAreaChannelPost

**Description** : *Represents a channel post*

**Layer** : 211

```tl
inputMediaAreaChannelPost#2271f2bf coordinates:MediaAreaCoordinates channel:InputChannel msg_id:int = MediaArea;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>coordinates</mark> | [`MediaAreaCoordinates`](type/MediaAreaCoordinates) | The size and location of the media area corresponding to the location sticker on top of the story media |
| <mark>channel</mark> | [`InputChannel`](type/InputChannel) | The channel that posted the message |
| <mark>msg_id</mark> | [`int`](type/int) | ID of the channel message |

---

## Type

[MediaArea](type/MediaArea)

---

## Example

```php
$mediaArea = $client->inputMediaAreaChannelPost(
	coordinates : $client->mediaAreaCoordinates(
		x : -1857423.576171875,
		y : -587124.912109375,
		w : 506042.9912109375,
		h : 1542777.65625,
		rotation : 1671381.8701171875,
		radius : 1121419.068359375,
	),
	channel : $client->inputChannelEmpty(),
	msg_id : 46,
);
```