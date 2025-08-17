# wallPaper

**Description** : *Represents a wallpaper based on an image*

**Layer** : 211

```tl
wallPaper#a437c3ed id:long flags:# creator:flags.0?true default:flags.1?true pattern:flags.3?true dark:flags.4?true access_hash:long slug:string document:Document settings:flags.2?WallPaperSettings = WallPaper;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Identifier |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **creator** | [`flags.0?true`](type/true) | Whether we created this wallpaper |
| **default** | [`flags.1?true`](type/true) | Whether this is the default wallpaper |
| **pattern** | [`flags.3?true`](type/true) | Whether this is a pattern wallpaper » |
| **dark** | [`flags.4?true`](type/true) | Whether this wallpaper should be used in dark mode |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash |
| <mark>slug</mark> | [`string`](type/string) | Unique wallpaper ID, used when generating wallpaper links or importing wallpaper links |
| <mark>document</mark> | [`Document`](type/Document) | The actual wallpaper |
| **settings** | [`flags.2?WallPaperSettings`](type/WallPaperSettings) | Info on how to generate the wallpaper, according to these instructions » |

---

## Type

[WallPaper](type/WallPaper)

---

## Example

```php
$wallPaper = $client->wallPaper(
	id : 1830565465792496366,
	creator : true,
	default : true,
	pattern : true,
	dark : true,
	access_hash : -4643331319758403631,
	slug : '4kUIbdyu23oilPq5',
	document : $client->documentEmpty(
		id : -5719053233722014607,
	),
	settings : $client->wallPaperSettings(
		blur : true,
		motion : true,
		background_color : 76,
		second_background_color : 84,
		third_background_color : 19,
		fourth_background_color : 71,
		intensity : 21,
		rotation : 3,
		emoticon : 'e7NtqkPi3ywJoO8v',
	),
);
```