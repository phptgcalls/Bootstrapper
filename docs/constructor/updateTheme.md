# updateTheme

**Description** : *A cloud theme was updated*

**Layer** : 211

```tl
updateTheme#8216fba3 theme:Theme = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>theme</mark> | [`Theme`](type/Theme) | Theme |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateTheme(
	theme : $client->theme(
		creator : true,
		default : true,
		for_chat : true,
		id : -4883658682454618852,
		access_hash : -6234151804302272868,
		slug : 'ifvK7jQ1FXDB4lPG',
		title : 'w1rnhBZgLDkRSlX0',
		document : $client->documentEmpty(
			id : 4354134225503428458,
		),
		settings : array(
			$client->themeSettings(
				message_colors_animated : true,
				base_theme : $client->baseThemeClassic(...),
				accent_color : 69,
				outbox_accent_color : 68,
				message_colors : array(0),
				wallpaper : $client->wallPaper(...),
			),
		),
		emoticon : 'oJtGBYXOfMij5bDK',
		installs_count : 61,
	),
);
```