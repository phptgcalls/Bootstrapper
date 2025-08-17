# messages.savedReactionTags

**Description** : *List of reaction tag » names assigned by the user*

**Layer** : 211

```tl
messages.savedReactionTags#3259950a tags:Vector<SavedReactionTag> hash:long = messages.SavedReactionTags;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>tags</mark> | [`Vector<SavedReactionTag>`](type/SavedReactionTag) | Saved reaction tags |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Type

[messages.SavedReactionTags](type/messages.SavedReactionTags)

---

## Example

```php
$messagesSavedReactionTags = $client->messages->savedReactionTags(
	tags : array(
		$client->savedReactionTag(
			reaction : $client->reactionEmpty(),
			title : 'DeRtlx4EIGhUFQnv',
			count : 57,
		),
	),
	hash : -7047490356168188065,
);
```