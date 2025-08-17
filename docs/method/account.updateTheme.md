# account.updateTheme

**Description** : *Update theme*

**Layer** : 211

```tl
account.updateTheme#2bf40ccc flags:# format:string theme:InputTheme slug:flags.0?string title:flags.1?string document:flags.2?InputDocument settings:flags.3?Vector<InputThemeSettings> = Theme;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>format</mark> | [`string`](type/string) | Theme format, a string that identifies the theming engines supported by the client |
| <mark>theme</mark> | [`InputTheme`](type/InputTheme) | Theme to update |
| **slug** | [`flags.0?string`](type/string) | Unique theme ID |
| **title** | [`flags.1?string`](type/string) | Theme name |
| **document** | [`flags.2?InputDocument`](type/InputDocument) | Theme file |
| **settings** | [`flags.3?Vector<InputThemeSettings>`](type/InputThemeSettings) | Theme settings |

---

## Result

[Theme](type/Theme)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **THEME_INVALID** | `400` | Invalid theme provided |

---

## Example

```php
$theme = $client->account->updateTheme(
	format : 'HQUqrvFukCwBX6tg',
	theme : $client->inputTheme(
		id : -3811839775798741368,
		access_hash : 716444397703446452,
	),
	slug : 'pMDeTKyjWkISxzV4',
	title : 'UKtXVFuaBCrywzgp',
	document : $client->inputDocumentEmpty(),
	settings : array(
		$client->inputThemeSettings(
			message_colors_animated : true,
			base_theme : $client->baseThemeClassic(),
			accent_color : 81,
			outbox_accent_color : 91,
			message_colors : array(1),
			wallpaper : $client->inputWallPaper(
				id : -2505369298380870405,
				access_hash : 8014361462441110010,
			),
			wallpaper_settings : $client->wallPaperSettings(
				blur : true,
				motion : true,
				background_color : 31,
				second_background_color : 31,
				third_background_color : 12,
				fourth_background_color : 26,
				intensity : 24,
				rotation : 36,
				emoticon : '6mNcKAUTEIBfq0W1',
			),
		),
	),
);
```