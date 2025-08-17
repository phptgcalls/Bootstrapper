# account.wallPapers

**Description** : *Installed wallpapers*

**Layer** : 211

```tl
account.wallPapers#cdc3858c hash:long wallpapers:Vector<WallPaper> = account.WallPapers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>wallpapers</mark> | [`Vector<WallPaper>`](type/WallPaper) | Wallpapers |

---

## Type

[account.WallPapers](type/account.WallPapers)

---

## Example

```php
$accountWallPapers = $client->account->wallPapers(
	hash : -7417185196210339599,
	wallpapers : array(
		$client->wallPaper(
			id : 247407203224293529,
			creator : true,
			default : true,
			pattern : true,
			dark : true,
			access_hash : -6364363816487339732,
			slug : 'wEj5tpWvqbXDhRMo',
			document : $client->documentEmpty(
				id : 4857884521299488210,
			),
			settings : $client->wallPaperSettings(
				blur : true,
				motion : true,
				background_color : 0,
				second_background_color : 55,
				third_background_color : 66,
				fourth_background_color : 53,
				intensity : 96,
				rotation : 14,
				emoticon : 'UD2Qc0TNRFHoXOzm',
			),
		),
		$client->wallPaperNoFile(
			id : -4979486593316392658,
			default : true,
			dark : true,
			settings : $client->wallPaperSettings(
				blur : true,
				motion : true,
				background_color : 10,
				second_background_color : 48,
				third_background_color : 75,
				fourth_background_color : 24,
				intensity : 56,
				rotation : 100,
				emoticon : 'RphIDSvV610U7nZP',
			),
		),
	),
);
```