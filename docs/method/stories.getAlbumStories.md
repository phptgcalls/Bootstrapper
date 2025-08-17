# stories.getAlbumStories

**Layer** : 211

```tl
stories.getAlbumStories#ac806d61 peer:InputPeer album_id:int offset:int limit:int = stories.Stories;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | NOTHING |
| <mark>album_id</mark> | [`int`](type/int) | NOTHING |
| <mark>offset</mark> | [`int`](type/int) | NOTHING |
| <mark>limit</mark> | [`int`](type/int) | NOTHING |

---

## Result

[stories.Stories](type/stories.Stories)

---

## Example

```php
$storiesStories = $client->stories->getAlbumStories(
	peer : $client->inputPeerEmpty(),
	album_id : 23,
	offset : 87,
	limit : 65,
);
```