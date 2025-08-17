# channel

**Description** : *Channel/supergroup info*

**Layer** : 211

```tl
channel#fe685355 flags:# creator:flags.0?true left:flags.2?true broadcast:flags.5?true verified:flags.7?true megagroup:flags.8?true restricted:flags.9?true signatures:flags.11?true min:flags.12?true scam:flags.19?true has_link:flags.20?true has_geo:flags.21?true slowmode_enabled:flags.22?true call_active:flags.23?true call_not_empty:flags.24?true fake:flags.25?true gigagroup:flags.26?true noforwards:flags.27?true join_to_send:flags.28?true join_request:flags.29?true forum:flags.30?true flags2:# stories_hidden:flags2.1?true stories_hidden_min:flags2.2?true stories_unavailable:flags2.3?true signature_profiles:flags2.12?true autotranslation:flags2.15?true broadcast_messages_allowed:flags2.16?true monoforum:flags2.17?true forum_tabs:flags2.19?true id:long access_hash:flags.13?long title:string username:flags.6?string photo:ChatPhoto date:int restriction_reason:flags.9?Vector<RestrictionReason> admin_rights:flags.14?ChatAdminRights banned_rights:flags.15?ChatBannedRights default_banned_rights:flags.18?ChatBannedRights participants_count:flags.17?int usernames:flags2.0?Vector<Username> stories_max_id:flags2.4?int color:flags2.7?PeerColor profile_color:flags2.8?PeerColor emoji_status:flags2.9?EmojiStatus level:flags2.10?int subscription_until_date:flags2.11?int bot_verification_icon:flags2.13?long send_paid_messages_stars:flags2.14?long linked_monoforum_id:flags2.18?long = Chat;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **creator** | [`flags.0?true`](type/true) | Whether the current user is the creator of this channel |
| **left** | [`flags.2?true`](type/true) | Whether the current user has left or is not a member of this channel |
| **broadcast** | [`flags.5?true`](type/true) | Is this a channel? |
| **verified** | [`flags.7?true`](type/true) | Is this channel verified by telegram? |
| **megagroup** | [`flags.8?true`](type/true) | Is this a supergroup? Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **restricted** | [`flags.9?true`](type/true) | Whether viewing/writing in this channel for a reason (see restriction_reason) |
| **signatures** | [`flags.11?true`](type/true) | Whether signatures are enabled (channels) |
| **min** | [`flags.12?true`](type/true) | See min |
| **scam** | [`flags.19?true`](type/true) | This channel/supergroup is probably a scam Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **has_link** | [`flags.20?true`](type/true) | Whether this channel has a linked discussion group » (or this supergroup is a channel's discussion group). The actual ID of the linked channel/supergroup is contained in channelFull.linked_chat_id. Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **has_geo** | [`flags.21?true`](type/true) | Whether this chanel has a geoposition |
| **slowmode_enabled** | [`flags.22?true`](type/true) | Whether slow mode is enabled for groups to prevent flood in chat. Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **call_active** | [`flags.23?true`](type/true) | Whether a group call or livestream is currently active |
| **call_not_empty** | [`flags.24?true`](type/true) | Whether there's anyone in the group call or livestream |
| **fake** | [`flags.25?true`](type/true) | If set, this supergroup/channel was reported by many users as a fake or scam: be careful when interacting with it. Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **gigagroup** | [`flags.26?true`](type/true) | Whether this supergroup is a gigagroupChanges to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **noforwards** | [`flags.27?true`](type/true) | Whether this channel or group is protected, thus does not allow forwarding messages from it |
| **join_to_send** | [`flags.28?true`](type/true) | Whether a user needs to join the supergroup before they can send messages: can be false only for discussion groups », toggle using channels.toggleJoinToSendChanges to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **join_request** | [`flags.29?true`](type/true) | Whether a user's join request will have to be approved by administrators, toggle using channels.toggleJoinToSendChanges to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **forum** | [`flags.30?true`](type/true) | Whether this supergroup is a forum. Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| <mark>flags2</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **stories_hidden** | [`flags2.1?true`](type/true) | Whether we have hidden all stories posted by this channel » |
| **stories_hidden_min** | [`flags2.2?true`](type/true) | If set, indicates that the stories_hidden flag was not populated, and its value must cannot be relied on; use the previously cached value, or re-fetch the constructor using channels.getChannels to obtain the latest value of the stories_hidden flag |
| **stories_unavailable** | [`flags2.3?true`](type/true) | No stories from the channel are visible |
| **signature_profiles** | [`flags2.12?true`](type/true) | If set, messages sent by admins to this channel will link to the admin's profile (just like with groups) |
| **autotranslation** | [`flags2.15?true`](type/true) | NOTHING |
| **broadcast_messages_allowed** | [`flags2.16?true`](type/true) | NOTHING |
| **monoforum** | [`flags2.17?true`](type/true) | NOTHING |
| **forum_tabs** | [`flags2.19?true`](type/true) | NOTHING |
| <mark>id</mark> | [`long`](type/long) | ID of the channel, see here » for more info |
| **access_hash** | [`flags.13?long`](type/long) | Access hash, see here » for more info |
| <mark>title</mark> | [`string`](type/string) | Title |
| **username** | [`flags.6?string`](type/string) | Main active username |
| <mark>photo</mark> | [`ChatPhoto`](type/ChatPhoto) | Profile photo |
| <mark>date</mark> | [`int`](type/int) | Date when the user joined the supergroup/channel, or if the user isn't a member, its creation date |
| **restriction_reason** | [`flags.9?Vector<RestrictionReason>`](type/RestrictionReason) | Contains the reason why access to this channel must be restricted. Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **admin_rights** | [`flags.14?ChatAdminRights`](type/ChatAdminRights) | Admin rights of the user in this channel (see rights) |
| **banned_rights** | [`flags.15?ChatBannedRights`](type/ChatBannedRights) | Banned rights of the user in this channel (see rights) |
| **default_banned_rights** | [`flags.18?ChatBannedRights`](type/ChatBannedRights) | Default chat rights (see rights) |
| **participants_count** | [`flags.17?int`](type/int) | Participant count |
| **usernames** | [`flags2.0?Vector<Username>`](type/Username) | Additional usernames |
| **stories_max_id** | [`flags2.4?int`](type/int) | ID of the maximum read story |
| **color** | [`flags2.7?PeerColor`](type/PeerColor) | The channel's accent color |
| **profile_color** | [`flags2.8?PeerColor`](type/PeerColor) | The channel's profile color |
| **emoji_status** | [`flags2.9?EmojiStatus`](type/EmojiStatus) | Emoji status |
| **level** | [`flags2.10?int`](type/int) | Boost level. Changes to this flag should invalidate the local channelFull cache for this channel/supergroup ID, see here » for more info |
| **subscription_until_date** | [`flags2.11?int`](type/int) | Expiration date of the Telegram Star subscription » the current user has bought to gain access to this channel |
| **bot_verification_icon** | [`flags2.13?long`](type/long) | NOTHING |
| **send_paid_messages_stars** | [`flags2.14?long`](type/long) | NOTHING |
| **linked_monoforum_id** | [`flags2.18?long`](type/long) | NOTHING |

---

## Type

[Chat](type/Chat)

---

## Example

```php
$chat = $client->channel(
	creator : true,
	left : true,
	broadcast : true,
	verified : true,
	megagroup : true,
	restricted : true,
	signatures : true,
	min : true,
	scam : true,
	has_link : true,
	has_geo : true,
	slowmode_enabled : true,
	call_active : true,
	call_not_empty : true,
	fake : true,
	gigagroup : true,
	noforwards : true,
	join_to_send : true,
	join_request : true,
	forum : true,
	stories_hidden : true,
	stories_hidden_min : true,
	stories_unavailable : true,
	signature_profiles : true,
	autotranslation : true,
	broadcast_messages_allowed : true,
	monoforum : true,
	forum_tabs : true,
	id : -8271494839301729474,
	access_hash : -3713654194250289705,
	title : '5XncBz9VM1qxgW84',
	username : 'TakNone',
	photo : $client->chatPhotoEmpty(),
	date : 58,
	restriction_reason : array(
		$client->restrictionReason(
			platform : '2YMP1AwhSlRv0HGi',
			reason : 'vCHUbQ8j97s4aDgF',
			text : 'ncAXxKIH3OyQB7s2',
		),
	),
	admin_rights : $client->chatAdminRights(
		change_info : true,
		post_messages : true,
		edit_messages : true,
		delete_messages : true,
		ban_users : true,
		invite_users : true,
		pin_messages : true,
		add_admins : true,
		anonymous : true,
		manage_call : true,
		other : true,
		manage_topics : true,
		post_stories : true,
		edit_stories : true,
		delete_stories : true,
		manage_direct_messages : true,
	),
	banned_rights : $client->chatBannedRights(
		view_messages : true,
		send_messages : true,
		send_media : true,
		send_stickers : true,
		send_gifs : true,
		send_games : true,
		send_inline : true,
		embed_links : true,
		send_polls : true,
		change_info : true,
		invite_users : true,
		pin_messages : true,
		manage_topics : true,
		send_photos : true,
		send_videos : true,
		send_roundvideos : true,
		send_audios : true,
		send_voices : true,
		send_docs : true,
		send_plain : true,
		until_date : 24,
	),
	default_banned_rights : $client->chatBannedRights(
		view_messages : true,
		send_messages : true,
		send_media : true,
		send_stickers : true,
		send_gifs : true,
		send_games : true,
		send_inline : true,
		embed_links : true,
		send_polls : true,
		change_info : true,
		invite_users : true,
		pin_messages : true,
		manage_topics : true,
		send_photos : true,
		send_videos : true,
		send_roundvideos : true,
		send_audios : true,
		send_voices : true,
		send_docs : true,
		send_plain : true,
		until_date : 81,
	),
	participants_count : 73,
	usernames : array(
		$client->username(
			editable : true,
			active : true,
			username : 'TakNone',
		),
	),
	stories_max_id : 57,
	color : $client->peerColor(
		color : 81,
		background_emoji_id : -6962782780957776543,
	),
	profile_color : $client->peerColor(
		color : 48,
		background_emoji_id : -5942839725022298441,
	),
	emoji_status : $client->emojiStatusEmpty(),
	level : 13,
	subscription_until_date : 90,
	bot_verification_icon : 5596820753453380165,
	send_paid_messages_stars : 7064055529899465343,
	linked_monoforum_id : -6373315618492429090,
);
```