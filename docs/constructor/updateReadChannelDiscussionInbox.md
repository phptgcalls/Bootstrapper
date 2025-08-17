# updateReadChannelDiscussionInbox

**Description** : *Incoming comments in a discussion thread were marked as read*

**Layer** : 211

```tl
updateReadChannelDiscussionInbox#d6b19546 flags:# channel_id:long top_msg_id:int read_max_id:int broadcast_id:flags.0?long broadcast_post:flags.0?int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>channel_id</mark> | [`long`](type/long) | Discussion group ID |
| <mark>top_msg_id</mark> | [`int`](type/int) | ID of the group message that started the thread (message in linked discussion group) |
| <mark>read_max_id</mark> | [`int`](type/int) | Message ID of latest read incoming message for this thread |
| **broadcast_id** | [`flags.0?long`](type/long) | If set, contains the ID of the channel that contains the post that started the comment thread in the discussion group (channel_id) |
| **broadcast_post** | [`flags.0?int`](type/int) | If set, contains the ID of the channel post that started the comment thread |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateReadChannelDiscussionInbox(
	channel_id : -9176664091386638191,
	top_msg_id : 36,
	read_max_id : 52,
	broadcast_id : 7836854862708862657,
	broadcast_post : 89,
);
```