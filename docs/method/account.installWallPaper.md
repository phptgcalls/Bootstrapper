# account.installWallPaper

**Description** : *Install wallpaper*

**Layer** : 211

```tl
account.installWallPaper#feed5769 wallpaper:InputWallPaper settings:WallPaperSettings = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>wallpaper</mark> | [`InputWallPaper`](type/InputWallPaper) | Wallpaper to install |
| <mark>settings</mark> | [`WallPaperSettings`](type/WallPaperSettings) | Wallpaper settings |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **WALLPAPER_INVALID** | `400` | The specified wallpaper is invalid |

---

## Example

```php
$bool = $client->account->installWallPaper(
	wallpaper : $client->inputWallPaper(
		id : 577011778424070795,
		access_hash : 1502314440939944970,
	),
	settings : $client->wallPaperSettings(
		blur : true,
		motion : true,
		background_color : 80,
		second_background_color : 15,
		third_background_color : 48,
		fourth_background_color : 28,
		intensity : 15,
		rotation : 78,
		emoticon : '4VSgIeuZMOjmxJCk',
	),
);
```