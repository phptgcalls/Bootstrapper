# photos.deletePhotos

**Description** : *Deletes profile photos. The method returns a list of successfully deleted photo IDs*

**Layer** : 211

```tl
photos.deletePhotos#87cf7f2f id:Vector<InputPhoto> = Vector<long>;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`Vector<InputPhoto>`](type/InputPhoto) | Input photos to delete |

---

## Result

[Vector<long>](type/long)

---

## Example

```php
$long = $client->photos->deletePhotos(
	id : array(
		$client->inputPhotoEmpty(),
		$client->inputPhoto(
			id : 3994310531396539578,
			access_hash : -1396000781089939528,
			file_reference : 'h&??LiveProtoH?`??',
		),
	),
);
```