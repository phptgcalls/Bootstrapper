# foundStory

**Description** : *A story found using global story search »*

**Layer** : 211

```tl
foundStory#e87acbc0 peer:Peer story:StoryItem = FoundStory;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | The peer that posted the story |
| <mark>story</mark> | [`StoryItem`](type/StoryItem) | The story |

---

## Type

[FoundStory](type/FoundStory)

---

## Example

```php
$foundStory = $client->foundStory(
	peer : $client->peerUser(
		user_id : -1469401343825442271,
	),
	story : $client->storyItemDeleted(
		id : 57,
	),
);
```