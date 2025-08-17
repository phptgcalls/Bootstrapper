# premium.myBoosts

**Description** : *A list of peers we are currently boosting, and how many boost slots we have left*

**Layer** : 211

```tl
premium.myBoosts#9ae228e2 my_boosts:Vector<MyBoost> chats:Vector<Chat> users:Vector<User> = premium.MyBoosts;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>my_boosts</mark> | [`Vector<MyBoost>`](type/MyBoost) | Info about boosted peers and remaining boost slots |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Referenced chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Referenced users |

---

## Type

[premium.MyBoosts](type/premium.MyBoosts)

---

## Example

```php
$premiumMyBoosts = $client->premium->myBoosts(
	my_boosts : array(
		$client->myBoost(
			slot : 21,
			peer : $client->peerUser(
				user_id : 4884111024805861016,
			),
			date : 78,
			expires : 10,
			cooldown_until_date : 25,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 4203590088705877645,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -6890748631227645404,
			title : 'QrhbjFOA5uLN9BTY',
			photo : $client->chatPhotoEmpty(),
			participants_count : 99,
			date : 62,
			version : 31,
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
				until_date : 28,
			),
		),
		$client->chatForbidden(
			id : 1203427765053657584,
			title : 'lBvnuAkag4GSj9YZ',
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
			id : -5638975424156782096,
			access_hash : -9128427171625099309,
			title : 'NT5SxpcOhDFYkH9M',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 85,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'c1MYOjPDyU4GdKhH',
					reason : 'ONIgYC9H0VUGojXQ',
					text : 'aheHqZF04drnbSYX',
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
				until_date : 82,
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
				until_date : 26,
			),
			participants_count : 52,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 17,
			color : $client->peerColor(
				color : 51,
				background_emoji_id : -2596599581332720882,
			),
			profile_color : $client->peerColor(
				color : 71,
				background_emoji_id : 7162532805439760128,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 73,
			subscription_until_date : 53,
			bot_verification_icon : -2866724728438987715,
			send_paid_messages_stars : 962560524634500611,
			linked_monoforum_id : -3869151786664059717,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 7457099463110262498,
			access_hash : 4536291196016852927,
			title : 'sMWQORufyeCqo1F9',
			until_date : 48,
		),
	),
	users : array(
		$client->userEmpty(
			id : -8336581204103896724,
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
			id : 5192287262217688288,
			access_hash : -8104166942091917593,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 64,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'SlbNzgoYXWGkFcP5',
					reason : 'jQikKRlDUuJohngP',
					text : 'O2In5pWrJVYMbjGk',
				),
			),
			bot_inline_placeholder : '3wYCBrk49DJcqtEW',
			lang_code : 'JrLOfWTX18kSEpiI',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 55,
			color : $client->peerColor(
				color : 3,
				background_emoji_id : -2656005608859982228,
			),
			profile_color : $client->peerColor(
				color : 94,
				background_emoji_id : 9175793316394358785,
			),
			bot_active_users : 60,
			bot_verification_icon : 7229644344941651757,
			send_paid_messages_stars : -2075149438949102679,
		),
	),
);
```