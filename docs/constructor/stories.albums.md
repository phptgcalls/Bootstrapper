# stories.albums

**Layer** : 211

```tl
stories.albums#c3987a3a hash:long albums:Vector<StoryAlbum> = stories.Albums;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | NOTHING |
| <mark>albums</mark> | [`Vector<StoryAlbum>`](type/StoryAlbum) | NOTHING |

---

## Type

[stories.Albums](type/stories.Albums)

---

## Example

```php
$storiesAlbums = $client->stories->albums(
	hash : -4428584838575398634,
	albums : array(
		$client->storyAlbum(
			album_id : 38,
			title : 'pYrVbhOWytKgwnUi',
			icon_photo : $client->photoEmpty(
				id : 7361856322704438839,
			),
			icon_video : $client->documentEmpty(
				id : -8701830398808071586,
			),
		),
	),
);
```