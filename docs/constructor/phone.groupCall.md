# phone.groupCall

**Description** : *Contains info about a group call, and partial info about its participants*

**Layer** : 211

```tl
phone.groupCall#9e727aad call:GroupCall participants:Vector<GroupCallParticipant> participants_next_offset:string chats:Vector<Chat> users:Vector<User> = phone.GroupCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>call</mark> | [`GroupCall`](type/GroupCall) | Info about the group call |
| <mark>participants</mark> | [`Vector<GroupCallParticipant>`](type/GroupCallParticipant) | A partial list of participants |
| <mark>participants_next_offset</mark> | [`string`](type/string) | Next offset to use when fetching the remaining participants using phone.getGroupParticipants |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats mentioned in the participants vector |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users mentioned in the participants vector |

---

## Type

[phone.GroupCall](type/phone.GroupCall)

---

## Example

```php
$phoneGroupCall = $client->phone->groupCall(
	call : $client->groupCallDiscarded(
		id : -4586689211968028602,
		access_hash : 568735749260715965,
		duration : 8,
	),
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
				user_id : 2130716781305757244,
			),
			date : 96,
			active_date : 50,
			source : 97,
			volume : 66,
			about : 'fx9uVIseQbnA6l4Z',
			raise_hand_rating : -8367608172761792487,
			video : $client->groupCallParticipantVideo(
				paused : true,
				endpoint : 'ONgYrnzuAWMvK7fp',
				source_groups : array(
					$client->groupCallParticipantVideoSourceGroup(...),
				),
				audio_source : 96,
			),
			presentation : $client->groupCallParticipantVideo(
				paused : true,
				endpoint : 'XlE0wutDO8vp6bsV',
				source_groups : array(
					$client->groupCallParticipantVideoSourceGroup(...),
				),
				audio_source : 53,
			),
		),
	),
	participants_next_offset : 'xUA6q4TM81cdoYJi',
	chats : array(
		$client->chatEmpty(
			id : 6184122262364335750,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 2782963448878659237,
			title : 'W50fxYbje9phLr6z',
			photo : $client->chatPhotoEmpty(),
			participants_count : 41,
			date : 53,
			version : 37,
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
				until_date : 38,
			),
		),
		$client->chatForbidden(
			id : 4808966402619215446,
			title : 'MmFfGVjAlE9ihkYo',
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
			id : 9207213608821821645,
			access_hash : -4698482825019071463,
			title : 'CxRStrflhK79wD5B',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 1,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'EBtkR2ZKFeqn7iyd',
					reason : 'RPt20JmGorCXDAwy',
					text : 'Bs9zxOF3u2aMk5jS',
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
				until_date : 95,
			),
			participants_count : 81,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 27,
			color : $client->peerColor(
				color : 88,
				background_emoji_id : 3040627705801554670,
			),
			profile_color : $client->peerColor(
				color : 98,
				background_emoji_id : -299487493212215935,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 80,
			subscription_until_date : 100,
			bot_verification_icon : 7261282865560538900,
			send_paid_messages_stars : -4687219189202878884,
			linked_monoforum_id : -6359826104653815292,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 5546893090735049366,
			access_hash : -5927507424307088718,
			title : '4oiSOZ0zqyMg31xF',
			until_date : 28,
		),
	),
	users : array(
		$client->userEmpty(
			id : -6465251623558346203,
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
			id : -9150703576290066471,
			access_hash : -6377244898074140612,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 2,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'xqSfeD2Y8mhJgEyt',
					reason : '6xrbA5VLPX9lzHDR',
					text : 'Lx0CtMruTHQAOmY8',
				),
			),
			bot_inline_placeholder : 'Uo9Snr2s6aC0bziI',
			lang_code : 'VlMBLrawsHEUWG4C',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 37,
			color : $client->peerColor(
				color : 28,
				background_emoji_id : -3455138444118350768,
			),
			profile_color : $client->peerColor(
				color : 61,
				background_emoji_id : 8112164383772782721,
			),
			bot_active_users : 3,
			bot_verification_icon : -1284446242918578197,
			send_paid_messages_stars : -1313201774304009723,
		),
	),
);
```