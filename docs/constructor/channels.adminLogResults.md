# channels.adminLogResults

**Description** : *Admin log events*

**Layer** : 211

```tl
channels.adminLogResults#ed8af74d events:Vector<ChannelAdminLogEvent> chats:Vector<Chat> users:Vector<User> = channels.AdminLogResults;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>events</mark> | [`Vector<ChannelAdminLogEvent>`](type/ChannelAdminLogEvent) | Admin log events |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats mentioned in events |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users mentioned in events |

---

## Type

[channels.AdminLogResults](type/channels.AdminLogResults)

---

## Example

```php
$channelsAdminLogResults = $client->channels->adminLogResults(
	events : array(
		$client->channelAdminLogEvent(
			id : -3875403154109330917,
			date : 44,
			user_id : 4128913823025636957,
			action : $client->channelAdminLogEventActionChangeTitle(
				prev_value : 'abL1836O0ZvtTdsq',
				new_value : 'yvItg0zkDn4Sc6h2',
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 4926037793436159083,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -1747325121061883759,
			title : '3z0Bjp5ltR2C4hgs',
			photo : $client->chatPhotoEmpty(),
			participants_count : 97,
			date : 23,
			version : 79,
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
				until_date : 75,
			),
		),
		$client->chatForbidden(
			id : -5923020766624260927,
			title : 'uOqSDGjbWZ0aTkVg',
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
			id : 6060570631632199454,
			access_hash : -6179296657806224266,
			title : 'ASmWTbJFj8eyEMdz',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 6,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'lsTS94e1xAaIZ3Uu',
					reason : 'qwsVn7kD5KIXmP1U',
					text : 'oOBUnsQHL6wfJM9k',
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
				until_date : 5,
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
				until_date : 56,
			),
			participants_count : 99,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 33,
			color : $client->peerColor(
				color : 33,
				background_emoji_id : -7598455720759017670,
			),
			profile_color : $client->peerColor(
				color : 85,
				background_emoji_id : -2733123572854970751,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 92,
			subscription_until_date : 15,
			bot_verification_icon : -7525510659100521185,
			send_paid_messages_stars : -3840129063041042320,
			linked_monoforum_id : -9137240095128192326,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 4828370674867475457,
			access_hash : -8964707679040366261,
			title : '84dktu9Yv6CPSUBA',
			until_date : 76,
		),
	),
	users : array(
		$client->userEmpty(
			id : -2840645626787291892,
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
			id : -8518762003521241711,
			access_hash : -72710239787129117,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 80,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'cv8InHosLWU1r9ty',
					reason : 'ALurt3HYpOSkQMKU',
					text : 'ZxyTKYgPMQG2tsC1',
				),
			),
			bot_inline_placeholder : 'zdMYEcI983UVsNp4',
			lang_code : 'Zt5SzglEUuaGDNbA',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 91,
			color : $client->peerColor(
				color : 48,
				background_emoji_id : -5740317831591014320,
			),
			profile_color : $client->peerColor(
				color : 68,
				background_emoji_id : -5300415786888764839,
			),
			bot_active_users : 78,
			bot_verification_icon : 8523890533808353497,
			send_paid_messages_stars : 7906679143994565257,
		),
	),
);
```