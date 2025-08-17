# channelAdminLogEventActionChangeWallpaper

**Description** : *The wallpaper was changed*

**Layer** : 211

```tl
channelAdminLogEventActionChangeWallpaper#31bb5d52 prev_value:WallPaper new_value:WallPaper = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>prev_value</mark> | [`WallPaper`](type/WallPaper) | Previous wallpaper |
| <mark>new_value</mark> | [`WallPaper`](type/WallPaper) | New wallpaper |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionChangeWallpaper(
	prev_value : $client->wallPaper(
		id : 8280228132104043943,
		creator : true,
		default : true,
		pattern : true,
		dark : true,
		access_hash : -3354934026343792806,
		slug : 'nuX4jtUdB5bwhKC0',
		document : $client->documentEmpty(
			id : 7129241819991981296,
		),
		settings : $client->wallPaperSettings(
			blur : true,
			motion : true,
			background_color : 25,
			second_background_color : 71,
			third_background_color : 79,
			fourth_background_color : 90,
			intensity : 92,
			rotation : 100,
			emoticon : 'OsdHfATSeJKoqzb4',
		),
	),
	new_value : $client->wallPaper(
		id : 1371356738084521531,
		creator : true,
		default : true,
		pattern : true,
		dark : true,
		access_hash : 1861798472805901534,
		slug : 'Na7UImBdYXtSQ43D',
		document : $client->documentEmpty(
			id : -7034248005304026355,
		),
		settings : $client->wallPaperSettings(
			blur : true,
			motion : true,
			background_color : 23,
			second_background_color : 78,
			third_background_color : 90,
			fourth_background_color : 19,
			intensity : 95,
			rotation : 96,
			emoticon : 'zbV2FWn6j0pqLsS9',
		),
	),
);
```