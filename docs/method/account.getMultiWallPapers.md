# account.getMultiWallPapers

**Description** : *Get info about multiple wallpapers*

**Layer** : 211

```tl
account.getMultiWallPapers#65ad71dc wallpapers:Vector<InputWallPaper> = Vector<WallPaper>;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>wallpapers</mark> | [`Vector<InputWallPaper>`](type/InputWallPaper) | Wallpapers to fetch info about |

---

## Result

[Vector<WallPaper>](type/WallPaper)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **WALLPAPER_INVALID** | `400` | The specified wallpaper is invalid |

---

## Example

```php
$wallPaper = $client->account->getMultiWallPapers(
	wallpapers : array(
		$client->inputWallPaper(
			id : 7406433591018157700,
			access_hash : 2885507612140671624,
		),
		$client->inputWallPaperSlug(
			slug : 'gW5pCyeNho6wBK8E',
		),
		$client->inputWallPaperNoFile(
			id : -339316915747831680,
		),
	),
);
```