# chatlists.exportedInvites

**Description** : *Info about multiple chat folder deep links »*

**Layer** : 211

```tl
chatlists.exportedInvites#10ab6dc7 invites:Vector<ExportedChatlistInvite> chats:Vector<Chat> users:Vector<User> = chatlists.ExportedInvites;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>invites</mark> | [`Vector<ExportedChatlistInvite>`](type/ExportedChatlistInvite) | The chat folder deep links » |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Related chat information |
| <mark>users</mark> | [`Vector<User>`](type/User) | Related user information |

---

## Type

[chatlists.ExportedInvites](type/chatlists.ExportedInvites)

---

## Example

```php
$chatlistsExportedInvites = $client->chatlists->exportedInvites(
	invites : array(
		$client->exportedChatlistInvite(
			title : 'e7Y4imoqIwBDLGbQ',
			url : 'https://docs.liveproto.dev',
			peers : array(
				$client->peerUser(
					user_id : -3529423677920750339,
				),
				$client->peerChat(
					chat_id : -6602649676449067688,
				),
				$client->peerChannel(
					channel_id : -8908661736981385812,
				),
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 104441002079264183,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -2723482071338068916,
			title : 'CR8DH9GuJ15ei2cB',
			photo : $client->chatPhotoEmpty(),
			participants_count : 46,
			date : 48,
			version : 50,
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
				until_date : 96,
			),
		),
		$client->chatForbidden(
			id : -4615361159053836837,
			title : '7pLPAKgf4nzeYR3T',
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
			id : 5390662554107432922,
			access_hash : 5667566969036733940,
			title : '51uHyi3Ak4clmzJO',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 6,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'x5HCbTS9urlR6t8c',
					reason : 'BizPLJu4A85MpDsH',
					text : 'fCnIJp8ebc9QNiMB',
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
				until_date : 51,
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
				until_date : 24,
			),
			participants_count : 61,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 1,
			color : $client->peerColor(
				color : 31,
				background_emoji_id : 381879230414788388,
			),
			profile_color : $client->peerColor(
				color : 89,
				background_emoji_id : 683377763084854884,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 23,
			subscription_until_date : 90,
			bot_verification_icon : 8277052973852957514,
			send_paid_messages_stars : 3811117169231915030,
			linked_monoforum_id : 3357132656067498715,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 4712259058787561053,
			access_hash : -8088809679163830432,
			title : 'GFmiZjJvWY3UX9Ds',
			until_date : 43,
		),
	),
	users : array(
		$client->userEmpty(
			id : -6713402918217032632,
		),
		$client->user(
			self : true,
			contact : true,
			mutual_contact : true,
			deleted : true,
			bot : true,
			bot_chat_history : true,
			bot_nochats : true,
			verified : true,
			restricted : true,
			min : true,
			bot_inline_geo : true,
			support : true,
			scam : true,
			apply_min_photo : true,
			fake : true,
			bot_attach_menu : true,
			premium : true,
			attach_menu_enabled : true,
			bot_can_edit : true,
			close_friend : true,
			stories_hidden : true,
			stories_unavailable : true,
			contact_require_premium : true,
			bot_business : true,
			bot_has_main_app : true,
			id : -3822202938206500481,
			access_hash : 3481156886106432429,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 39,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'svSAT9dWnoRg8wUI',
					reason : 'xQ4igN9u6vqym0rc',
					text : 'muUaTYDQoliWqx2y',
				),
			),
			bot_inline_placeholder : 'ATDKNpmy9xE0dUco',
			lang_code : 'BXyr1SPINd8wYTFk',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 1,
			color : $client->peerColor(
				color : 69,
				background_emoji_id : 4274236525307904693,
			),
			profile_color : $client->peerColor(
				color : 75,
				background_emoji_id : 6827664353481521694,
			),
			bot_active_users : 3,
			bot_verification_icon : 752513646973473805,
			send_paid_messages_stars : 3605020058653710701,
		),
	),
);
```