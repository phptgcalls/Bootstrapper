# contacts.found

**Description** : *Users found by name substring and auxiliary data*

**Layer** : 211

```tl
contacts.found#b3134d9d my_results:Vector<Peer> results:Vector<Peer> chats:Vector<Chat> users:Vector<User> = contacts.Found;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>my_results</mark> | [`Vector<Peer>`](type/Peer) | Personalized results |
| <mark>results</mark> | [`Vector<Peer>`](type/Peer) | List of found user identifiers |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Found chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of users |

---

## Type

[contacts.Found](type/contacts.Found)

---

## Example

```php
$contactsFound = $client->contacts->found(
	my_results : array(
		$client->peerUser(
			user_id : -5500697510279972268,
		),
		$client->peerChat(
			chat_id : -2201660343424630938,
		),
		$client->peerChannel(
			channel_id : 9159788712342790426,
		),
	),
	results : array(
		$client->peerUser(
			user_id : 3880564594766848614,
		),
		$client->peerChat(
			chat_id : 2091364958546203458,
		),
		$client->peerChannel(
			channel_id : -3942892640461815228,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -6284306951187607387,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -852225360428828452,
			title : 'G86xeZFQTEpBH2JC',
			photo : $client->chatPhotoEmpty(),
			participants_count : 33,
			date : 76,
			version : 91,
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
				until_date : 61,
			),
		),
		$client->chatForbidden(
			id : -709754287541336786,
			title : 'yrBvH2V463EunWYZ',
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
			id : -6797757713457291870,
			access_hash : -249997456088199036,
			title : 'pyE1MtqTx3j7Vzi2',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 85,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'tPwbVzxDC5BgoFse',
					reason : 'BjTlM5w2kCHdALpb',
					text : '63hsKoxSbnTBtfvk',
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
				until_date : 75,
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
				until_date : 64,
			),
			participants_count : 84,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 1,
			color : $client->peerColor(
				color : 36,
				background_emoji_id : -8762168227807202083,
			),
			profile_color : $client->peerColor(
				color : 86,
				background_emoji_id : 7849145384101875129,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 51,
			subscription_until_date : 51,
			bot_verification_icon : -2313059900783696387,
			send_paid_messages_stars : -740739308322018348,
			linked_monoforum_id : -5743128351316386974,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -8647923136576675144,
			access_hash : -7951836225524553602,
			title : 'zHlQJCjsrKon2bay',
			until_date : 47,
		),
	),
	users : array(
		$client->userEmpty(
			id : 548964841151962316,
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
			id : -6693714140044134721,
			access_hash : -7469900369545632943,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 20,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'bTPHg5GdKjCDVtqk',
					reason : 'JUYEebxyQjv57ZIO',
					text : 'J795eOH3bQi0qosB',
				),
			),
			bot_inline_placeholder : 'EOrRkd7ztXHILwmK',
			lang_code : 'xIUiNSojvOGTCy2t',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 4,
			color : $client->peerColor(
				color : 5,
				background_emoji_id : -6277270090484877321,
			),
			profile_color : $client->peerColor(
				color : 73,
				background_emoji_id : 6723046348871050298,
			),
			bot_active_users : 90,
			bot_verification_icon : -4789811776481797580,
			send_paid_messages_stars : -133802843761364134,
		),
	),
);
```