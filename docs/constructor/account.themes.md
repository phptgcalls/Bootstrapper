# account.themes

**Description** : *Installed themes*

**Layer** : 211

```tl
account.themes#9a3d8c6d hash:long themes:Vector<Theme> = account.Themes;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>themes</mark> | [`Vector<Theme>`](type/Theme) | Themes |

---

## Type

[account.Themes](type/account.Themes)

---

## Example

```php
$accountThemes = $client->account->themes(
	hash : 5611240775035377917,
	themes : array(
		$client->theme(
			creator : true,
			default : true,
			for_chat : true,
			id : 488449833897631687,
			access_hash : -3988658218314773388,
			slug : 'RcCE3TiGYn5BwWNJ',
			title : 'vA1cYUPjZNLb6w4V',
			document : $client->documentEmpty(
				id : 5741601981544664078,
			),
			settings : array(
				$client->themeSettings(
					message_colors_animated : true,
					base_theme : $client->baseThemeClassic(...),
					accent_color : 61,
					outbox_accent_color : 14,
					message_colors : array(20),
					wallpaper : $client->wallPaper(...),
				),
			),
			emoticon : 'BEPsRSlcf9yrDTNx',
			installs_count : 42,
		),
	),
);
```