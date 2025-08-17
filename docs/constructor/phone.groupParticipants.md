# phone.groupParticipants

**Description** : *Info about the participants of a group call or livestream*

**Layer** : 211

```tl
phone.groupParticipants#f47751b6 count:int participants:Vector<GroupCallParticipant> next_offset:string chats:Vector<Chat> users:Vector<User> version:int = phone.GroupParticipants;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Number of participants |
| <mark>participants</mark> | [`Vector<GroupCallParticipant>`](type/GroupCallParticipant) | List of participants |
| <mark>next_offset</mark> | [`string`](type/string) | If not empty, the specified list of participants is partial, and more participants can be fetched specifying this parameter as offset in phone.getGroupParticipants |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |
| <mark>version</mark> | [`int`](type/int) | Version info |

---

## Type

[phone.GroupParticipants](type/phone.GroupParticipants)

---

## Example

```php
$phoneGroupParticipants = $client->phone->groupParticipants(
	count : 72,
	participants : array(
		$client->groupCallParticipant(
			muted : true,
			left : true,
			can_self_unmute : true,
			just_joined : true,
			versioned : true,
			min : true,
			muted_by_you : true,
			volume_by_admin : true,
			self : true,
			video_joined : true,
			peer : $client->peerUser(
				user_id : 6702293867550838555,
			),
			date : 12,
			active_date : 65,
			source : 66,
			volume : 100,
			about : 'rcPzgsGj4J7RZqVQ',
			raise_hand_rating : -7116966823639766624,
			video : $client->groupCallParticipantVideo(
				paused : true,
				endpoint : '0REmWFfoS1xHbjUn',
				source_groups : array(
					$client->groupCallParticipantVideoSourceGroup(...),
				),
				audio_source : 60,
			),
			presentation : $client->groupCallParticipantVideo(
				paused : true,
				endpoint : 'NQ3c4VZ57WLpyhzb',
				source_groups : array(
					$client->groupCallParticipantVideoSourceGroup(...),
				),
				audio_source : 11,
			),
		),
	),
	next_offset : 'fOK8nU2kFAybPlvs',
	chats : array(
		$client->chatEmpty(
			id : -6044856714697463024,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -2176216902896688130,
			title : '1aXtQbmELCz96Kwj',
			photo : $client->chatPhotoEmpty(),
			participants_count : 25,
			date : 65,
			version : 13,
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
				until_date : 2,
			),
		),
		$client->chatForbidden(
			id : -6529728523789633807,
			title : 'tsaxBy6vRbEqgVJC',
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
			id : -7082639347050240155,
			access_hash : 2317775400267086277,
			title : 'zXNxsEICSiFl96VU',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 82,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'CG2MhodHDn60bgXL',
					reason : 'z9NaumVds0MZ5CAH',
					text : 'tT7wL0ukiEsncdeY',
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
				until_date : 49,
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
				until_date : 0,
			),
			participants_count : 65,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 11,
			color : $client->peerColor(
				color : 65,
				background_emoji_id : 7286180243845585044,
			),
			profile_color : $client->peerColor(
				color : 97,
				background_emoji_id : 29829213659117616,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 2,
			subscription_until_date : 19,
			bot_verification_icon : -4626420979836216930,
			send_paid_messages_stars : -408477316116128756,
			linked_monoforum_id : 4047123404360637047,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -15346420099638150,
			access_hash : 6065431852567379663,
			title : 'qH8ahQEtPv5ckDIV',
			until_date : 30,
		),
	),
	users : array(
		$client->userEmpty(
			id : 8899557751250107616,
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
			id : 8229563931370842274,
			access_hash : -5492439066943405899,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 66,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'f9Tv8xLOjZh6egAR',
					reason : 'dO0xEBQbGk1XqvaU',
					text : '3bxfPR6jAeXZlKha',
				),
			),
			bot_inline_placeholder : 'YUjFukmKhrTwA5yO',
			lang_code : 'O5bNmHEzpC6su9XU',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 56,
			color : $client->peerColor(
				color : 55,
				background_emoji_id : 8165108092407875924,
			),
			profile_color : $client->peerColor(
				color : 62,
				background_emoji_id : -2733594078658454421,
			),
			bot_active_users : 2,
			bot_verification_icon : 1148887462888968608,
			send_paid_messages_stars : -2471797820541667753,
		),
	),
	version : 90,
);
```