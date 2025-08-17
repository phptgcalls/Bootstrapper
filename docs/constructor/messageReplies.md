# messageReplies

**Description** : *Info about the comment section of a channel post, or a simple message thread*

**Layer** : 211

```tl
messageReplies#83d60fc2 flags:# comments:flags.0?true replies:int replies_pts:int recent_repliers:flags.1?Vector<Peer> channel_id:flags.0?long max_id:flags.2?int read_max_id:flags.3?int = MessageReplies;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **comments** | [`flags.0?true`](type/true) | Whether this constructor contains information about the comment section of a channel post, or a simple message thread |
| <mark>replies</mark> | [`int`](type/int) | Contains the total number of replies in this thread or comment section |
| <mark>replies_pts</mark> | [`int`](type/int) | PTS of the message that started this thread |
| **recent_repliers** | [`flags.1?Vector<Peer>`](type/Peer) | For channel post comments, contains information about the last few comment posters for a specific thread, to show a small list of commenter profile pictures in client previews |
| **channel_id** | [`flags.0?long`](type/long) | For channel post comments, contains the ID of the associated discussion supergroup |
| **max_id** | [`flags.2?int`](type/int) | ID of the latest message in this thread or comment section |
| **read_max_id** | [`flags.3?int`](type/int) | Contains the ID of the latest read message in this thread or comment section |

---

## Type

[MessageReplies](type/MessageReplies)

---

## Example

```php
$messageReplies = $client->messageReplies(
	comments : true,
	replies : 80,
	replies_pts : 6,
	recent_repliers : array(
		$client->peerUser(
			user_id : -1860455050773795201,
		),
		$client->peerChat(
			chat_id : 1200211381671397567,
		),
		$client->peerChannel(
			channel_id : -1502901559336723616,
		),
	),
	channel_id : -2373439834865467916,
	max_id : 6,
	read_max_id : 89,
);
```