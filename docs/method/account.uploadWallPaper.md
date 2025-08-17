# account.uploadWallPaper

**Description** : *Create and upload a new wallpaper*

**Layer** : 211

```tl
account.uploadWallPaper#e39a8f03 flags:# for_chat:flags.0?true file:InputFile mime_type:string settings:WallPaperSettings = WallPaper;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **for_chat** | [`flags.0?true`](type/true) | Set this flag when uploading wallpapers to be passed to messages.setChatWallPaper |
| <mark>file</mark> | [`InputFile`](type/InputFile) | The JPG/PNG wallpaper |
| <mark>mime_type</mark> | [`string`](type/string) | MIME type of uploaded wallpaper |
| <mark>settings</mark> | [`WallPaperSettings`](type/WallPaperSettings) | Wallpaper settings |

---

## Result

[WallPaper](type/WallPaper)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **WALLPAPER_FILE_INVALID** | `400` | The specified wallpaper file is invalid |
| **WALLPAPER_MIME_INVALID** | `400` | The specified wallpaper MIME type is invalid |

---

## Example

```php
$wallPaper = $client->account->uploadWallPaper(
	for_chat : true,
	file : $client->inputFile(
		id : 3891754805496957142,
		parts : 13,
		name : '72K4lywQ0DzvhmM1',
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
	),
	mime_type : 'vYkoKdHA78ix2GmN',
	settings : $client->wallPaperSettings(
		blur : true,
		motion : true,
		background_color : 73,
		second_background_color : 23,
		third_background_color : 11,
		fourth_background_color : 2,
		intensity : 51,
		rotation : 16,
		emoticon : '8kpxQX1b2avSIM3R',
	),
);
```