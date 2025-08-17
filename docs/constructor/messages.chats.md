# messages.chats

**Description** : *List of chats with auxiliary data*

**Layer** : 211

```tl
messages.chats#64ff9fd5 chats:Vector<Chat> = messages.Chats;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | List of chats |

---

## Type

[messages.Chats](type/messages.Chats)

---

## Example

```php
$messagesChats = $client->messages->chats(
	chats : array(
		$client->chatEmpty(
			id : 2637580828372583768,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 1255727557485466313,
			title : 'diQ7q2b1hto3HLPZ',
			photo : $client->chatPhotoEmpty(),
			participants_count : 32,
			date : 27,
			version : 22,
			migrated_to : $client->inputChannelEmpty(),
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
				until_date : 25,
			),
		),
		$client->chatForbidden(
			id : -8036709972138463710,
			title : 'JzEQOLgIC2j3tkNY',
		),
		$client->channel(
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
			id : 7507393576233655960,
			access_hash : 5914342282370900663,
			title : 'bLuPl7HxDjIpsCAv',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 64,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'tZbryAu1BIavxeXH',
					reason : 'l9ahzn2LYRCTEKOb',
					text : '1TU7nfvWPo2LHjkp',
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
				until_date : 74,
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
				until_date : 6,
			),
			participants_count : 22,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 12,
			color : $client->peerColor(
				color : 92,
				background_emoji_id : -6585218190142047517,
			),
			profile_color : $client->peerColor(
				color : 61,
				background_emoji_id : -7461201546522282420,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 13,
			subscription_until_date : 33,
			bot_verification_icon : -1971612603783793859,
			send_paid_messages_stars : 1750294595799819171,
			linked_monoforum_id : 1845646282401009024,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -2090875361435552617,
			access_hash : -619927276004332821,
			title : 'cVTvDd9O7360bBsw',
			until_date : 69,
		),
	),
);
```