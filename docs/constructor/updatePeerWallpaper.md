# updatePeerWallpaper

**Description** : *The wallpaper » of a given peer has changed*

**Layer** : 211

```tl
updatePeerWallpaper#ae3f101d flags:# wallpaper_overridden:flags.1?true peer:Peer wallpaper:flags.0?WallPaper = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **wallpaper_overridden** | [`flags.1?true`](type/true) | Whether the other user has chosen a custom wallpaper for us using messages.setChatWallPaper and the for_both flag, see here » for more info |
| <mark>peer</mark> | [`Peer`](type/Peer) | The peer where the wallpaper has changed |
| **wallpaper** | [`flags.0?WallPaper`](type/WallPaper) | The new wallpaper, if none the wallpaper was removed and the default wallpaper should be used |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updatePeerWallpaper(
	wallpaper_overridden : true,
	peer : $client->peerUser(
		user_id : 8713819606066459626,
	),
	wallpaper : $client->wallPaper(
		id : -6464700897308000409,
		creator : true,
		default : true,
		pattern : true,
		dark : true,
		access_hash : 8205491615644862868,
		slug : '4tWfe1MDACnLbBFR',
		document : $client->documentEmpty(
			id : 2510371929849259046,
		),
		settings : $client->wallPaperSettings(
			blur : true,
			motion : true,
			background_color : 52,
			second_background_color : 89,
			third_background_color : 57,
			fourth_background_color : 79,
			intensity : 27,
			rotation : 4,
			emoticon : 'BFMj7HfhndLtEiRN',
		),
	),
);
```