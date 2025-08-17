# messageReplyStoryHeader

**Description** : *Represents a reply to a story*

**Layer** : 211

```tl
messageReplyStoryHeader#e5af939 peer:Peer story_id:int = MessageReplyHeader;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | Sender of the story |
| <mark>story_id</mark> | [`int`](type/int) | Story ID |

---

## Type

[MessageReplyHeader](type/MessageReplyHeader)

---

## Example

```php
$messageReplyHeader = $client->messageReplyStoryHeader(
	peer : $client->peerUser(
		user_id : -8983638390235371529,
	),
	story_id : 33,
);
```