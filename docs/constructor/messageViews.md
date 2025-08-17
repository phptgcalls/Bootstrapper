# messageViews

**Description** : *View, forward counter + info about replies of a specific message*

**Layer** : 211

```tl
messageViews#455b853d flags:# views:flags.0?int forwards:flags.1?int replies:flags.2?MessageReplies = MessageViews;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **views** | [`flags.0?int`](type/int) | View count of message |
| **forwards** | [`flags.1?int`](type/int) | Forward count of message |
| **replies** | [`flags.2?MessageReplies`](type/MessageReplies) | Reply and thread information of message |

---

## Type

[MessageViews](type/MessageViews)

---

## Example

```php
$messageViews = $client->messageViews(
	views : 76,
	forwards : 67,
	replies : $client->messageReplies(
		comments : true,
		replies : 12,
		replies_pts : 68,
		recent_repliers : array(
			$client->peerUser(
				user_id : 3974114538719799669,
			),
			$client->peerChat(
				chat_id : -5041882106838959644,
			),
			$client->peerChannel(
				channel_id : -2259406577327089357,
			),
		),
		channel_id : 6250409452928794425,
		max_id : 100,
		read_max_id : 100,
	),
);
```