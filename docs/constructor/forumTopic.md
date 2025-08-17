# forumTopic

**Description** : *Represents a forum topic*

**Layer** : 211

```tl
forumTopic#71701da9 flags:# my:flags.1?true closed:flags.2?true pinned:flags.3?true short:flags.5?true hidden:flags.6?true id:int date:int title:string icon_color:int icon_emoji_id:flags.0?long top_message:int read_inbox_max_id:int read_outbox_max_id:int unread_count:int unread_mentions_count:int unread_reactions_count:int from_id:Peer notify_settings:PeerNotifySettings draft:flags.4?DraftMessage = ForumTopic;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **my** | [`flags.1?true`](type/true) | Whether the topic was created by the current user |
| **closed** | [`flags.2?true`](type/true) | Whether the topic is closed (no messages can be sent to it) |
| **pinned** | [`flags.3?true`](type/true) | Whether the topic is pinned |
| **short** | [`flags.5?true`](type/true) | Whether this constructor is a reduced version of the full topic information. If set, only the my, closed, id, date, title, icon_color, icon_emoji_id and from_id parameters will contain valid information. Reduced info is usually only returned in topic-related admin log events » and in the messages.channelMessages constructor: if needed, full information can be fetched using channels.getForumTopicsByID |
| **hidden** | [`flags.6?true`](type/true) | Whether the topic is hidden (only valid for the "General" topic, id=1) |
| <mark>id</mark> | [`int`](type/int) | Topic ID |
| <mark>date</mark> | [`int`](type/int) | Topic creation date |
| <mark>title</mark> | [`string`](type/string) | Topic title |
| <mark>icon_color</mark> | [`int`](type/int) | If no custom emoji icon is specified, specifies the color of the fallback topic icon (RGB), one of 0x6FB9F0, 0xFFD67E, 0xCB86DB, 0x8EEE98, 0xFF93B2, or 0xFB6F5F |
| **icon_emoji_id** | [`flags.0?long`](type/long) | ID of the custom emoji used as topic icon |
| <mark>top_message</mark> | [`int`](type/int) | ID of the last message that was sent to this topic |
| <mark>read_inbox_max_id</mark> | [`int`](type/int) | Position up to which all incoming messages are read |
| <mark>read_outbox_max_id</mark> | [`int`](type/int) | Position up to which all outgoing messages are read |
| <mark>unread_count</mark> | [`int`](type/int) | Number of unread messages |
| <mark>unread_mentions_count</mark> | [`int`](type/int) | Number of unread mentions |
| <mark>unread_reactions_count</mark> | [`int`](type/int) | Number of unread reactions to messages you sent |
| <mark>from_id</mark> | [`Peer`](type/Peer) | ID of the peer that created the topic |
| <mark>notify_settings</mark> | [`PeerNotifySettings`](type/PeerNotifySettings) | Notification settings |
| **draft** | [`flags.4?DraftMessage`](type/DraftMessage) | Message draft |

---

## Type

[ForumTopic](type/ForumTopic)

---

## Example

```php
$forumTopic = $client->forumTopic(
	my : true,
	closed : true,
	pinned : true,
	short : true,
	hidden : true,
	id : 28,
	date : 29,
	title : '6719RpXAyzT3SGwt',
	icon_color : 3,
	icon_emoji_id : -6383882652701839274,
	top_message : 43,
	read_inbox_max_id : 33,
	read_outbox_max_id : 4,
	unread_count : 49,
	unread_mentions_count : 82,
	unread_reactions_count : 56,
	from_id : $client->peerUser(
		user_id : -3924186710965237674,
	),
	notify_settings : $client->peerNotifySettings(
		show_previews : $client->boolFalse(),
		silent : $client->boolFalse(),
		mute_until : 78,
		ios_sound : $client->notificationSoundDefault(),
		android_sound : $client->notificationSoundDefault(),
		other_sound : $client->notificationSoundDefault(),
		stories_muted : $client->boolFalse(),
		stories_hide_sender : $client->boolFalse(),
		stories_ios_sound : $client->notificationSoundDefault(),
		stories_android_sound : $client->notificationSoundDefault(),
		stories_other_sound : $client->notificationSoundDefault(),
	),
	draft : $client->draftMessageEmpty(
		date : 90,
	),
);
```