# account.autoSaveSettings

**Description** : *Contains media autosave settings*

**Layer** : 211

```tl
account.autoSaveSettings#4c3e069d users_settings:AutoSaveSettings chats_settings:AutoSaveSettings broadcasts_settings:AutoSaveSettings exceptions:Vector<AutoSaveException> chats:Vector<Chat> users:Vector<User> = account.AutoSaveSettings;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>users_settings</mark> | [`AutoSaveSettings`](type/AutoSaveSettings) | Default media autosave settings for private chats |
| <mark>chats_settings</mark> | [`AutoSaveSettings`](type/AutoSaveSettings) | Default media autosave settings for groups and supergroups |
| <mark>broadcasts_settings</mark> | [`AutoSaveSettings`](type/AutoSaveSettings) | Default media autosave settings for channels |
| <mark>exceptions</mark> | [`Vector<AutoSaveException>`](type/AutoSaveException) | Peer-specific granular autosave settings |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats mentioned in the peer-specific granular autosave settings |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users mentioned in the peer-specific granular autosave settings |

---

## Type

[account.AutoSaveSettings](type/account.AutoSaveSettings)

---

## Example

```php
$accountAutoSaveSettings = $client->account->autoSaveSettings(
	users_settings : $client->autoSaveSettings(
		photos : true,
		videos : true,
		video_max_size : 5243074576538584811,
	),
	chats_settings : $client->autoSaveSettings(
		photos : true,
		videos : true,
		video_max_size : 2872062158033414354,
	),
	broadcasts_settings : $client->autoSaveSettings(
		photos : true,
		videos : true,
		video_max_size : -2818386401759105238,
	),
	exceptions : array(
		$client->autoSaveException(
			peer : $client->peerUser(
				user_id : -255759694896392455,
			),
			settings : $client->autoSaveSettings(
				photos : true,
				videos : true,
				video_max_size : 3113036349733264845,
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 2812415804022479062,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -2048337512761973254,
			title : 'GXkj5x76oIAiC3pB',
			photo : $client->chatPhotoEmpty(),
			participants_count : 65,
			date : 87,
			version : 21,
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
				until_date : 20,
			),
		),
		$client->chatForbidden(
			id : 374268324155348914,
			title : 'NIbe314LMVWw5ihT',
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
			id : -6767867807879563128,
			access_hash : -7504621216117277084,
			title : '1NZAlqfrP9hUxi5O',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 9,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '2DW94O3kT1fxqoPS',
					reason : 'aweb9KMAvV1n86DP',
					text : 'xvAieroPHWCV7Rq4',
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
				until_date : 10,
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
				until_date : 87,
			),
			participants_count : 12,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 36,
			color : $client->peerColor(
				color : 6,
				background_emoji_id : -9020929592845585362,
			),
			profile_color : $client->peerColor(
				color : 34,
				background_emoji_id : 3764652624782662515,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 93,
			subscription_until_date : 21,
			bot_verification_icon : -7640683885755446592,
			send_paid_messages_stars : 4054950461722595056,
			linked_monoforum_id : 1871131419161153505,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -5469824925960746852,
			access_hash : -4132180867875220358,
			title : 'UaYow9HhVTvxzt6k',
			until_date : 67,
		),
	),
	users : array(
		$client->userEmpty(
			id : 8823070052543545378,
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
			id : 8001932234361256307,
			access_hash : -531426541409110521,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 30,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'pHczo4KZwSyVfBUI',
					reason : 'SDI1drZNwOVJgA8f',
					text : 'XShZ9WYe0Ntpzwys',
				),
			),
			bot_inline_placeholder : 'pKsjnMVfy8gQ1A5o',
			lang_code : 'V5KWACyURMxpB2nh',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 49,
			color : $client->peerColor(
				color : 91,
				background_emoji_id : 1375227659545852600,
			),
			profile_color : $client->peerColor(
				color : 1,
				background_emoji_id : -4547960621440344857,
			),
			bot_active_users : 76,
			bot_verification_icon : 6691523063592585745,
			send_paid_messages_stars : 8757510243576215990,
		),
	),
);
```