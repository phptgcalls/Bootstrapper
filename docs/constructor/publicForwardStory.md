# publicForwardStory

**Description** : *Contains info about a forward of a story as a repost by a public channel*

**Layer** : 211

```tl
publicForwardStory#edf3add0 peer:Peer story:StoryItem = PublicForward;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | The channel that reposted the story |
| <mark>story</mark> | [`StoryItem`](type/StoryItem) | The reposted story (may be different from the original story) |

---

## Type

[PublicForward](type/PublicForward)

---

## Example

```php
$publicForward = $client->publicForwardStory(
	peer : $client->peerUser(
		user_id : -4048915333166172407,
	),
	story : $client->storyItemDeleted(
		id : 60,
	),
);
```