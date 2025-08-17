# account.createTheme

**Description** : *Create a theme*

**Layer** : 211

```tl
account.createTheme#652e4400 flags:# slug:string title:string document:flags.2?InputDocument settings:flags.3?Vector<InputThemeSettings> = Theme;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>slug</mark> | [`string`](type/string) | Unique theme ID used to generate theme deep links, can be empty to autogenerate a random ID |
| <mark>title</mark> | [`string`](type/string) | Theme name |
| **document** | [`flags.2?InputDocument`](type/InputDocument) | Theme file |
| **settings** | [`flags.3?Vector<InputThemeSettings>`](type/InputThemeSettings) | Theme settings, multiple values can be provided for the different base themes (day/night mode, etc) |

---

## Result

[Theme](type/Theme)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **THEME_MIME_INVALID** | `400` | The theme's MIME type is invalid |
| **THEME_TITLE_INVALID** | `400` | The specified theme title is invalid |

---

## Example

```php
$theme = $client->account->createTheme(
	slug : '198gdNRIsyY3iTeH',
	title : 'ieDvY540tgHEp2dX',
	document : $client->inputDocumentEmpty(),
	settings : array(
		$client->inputThemeSettings(
			message_colors_animated : true,
			base_theme : $client->baseThemeClassic(),
			accent_color : 88,
			outbox_accent_color : 58,
			message_colors : array(90),
			wallpaper : $client->inputWallPaper(
				id : -639068923310036421,
				access_hash : -692818282996057778,
			),
			wallpaper_settings : $client->wallPaperSettings(
				blur : true,
				motion : true,
				background_color : 97,
				second_background_color : 29,
				third_background_color : 53,
				fourth_background_color : 52,
				intensity : 61,
				rotation : 49,
				emoticon : '28uaSNgAlhtoywrL',
			),
		),
	),
);
```