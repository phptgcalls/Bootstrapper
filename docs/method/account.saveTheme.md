# account.saveTheme

**Description** : *Save a theme*

**Layer** : 211

```tl
account.saveTheme#f257106c theme:InputTheme unsave:Bool = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>theme</mark> | [`InputTheme`](type/InputTheme) | Theme to save |
| <mark>unsave</mark> | [`Bool`](type/Bool) | Unsave |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **THEME_INVALID** | `400` | Invalid theme provided |

---

## Example

```php
$bool = $client->account->saveTheme(
	theme : $client->inputTheme(
		id : 1875353253622741892,
		access_hash : -8964458379426262972,
	),
	unsave : $client->boolFalse(),
);
```