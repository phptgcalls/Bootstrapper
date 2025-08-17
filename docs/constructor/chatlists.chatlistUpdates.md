# chatlists.chatlistUpdates

**Description** : *Updated information about a chat folder deep link »*

**Layer** : 211

```tl
chatlists.chatlistUpdates#93bd878d missing_peers:Vector<Peer> chats:Vector<Chat> users:Vector<User> = chatlists.ChatlistUpdates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>missing_peers</mark> | [`Vector<Peer>`](type/Peer) | New peers to join |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Related chat information |
| <mark>users</mark> | [`Vector<User>`](type/User) | Related user information |

---

## Type

[chatlists.ChatlistUpdates](type/chatlists.ChatlistUpdates)

---

## Example

```php
$chatlistsChatlistUpdates = $client->chatlists->chatlistUpdates(
	missing_peers : array(
		$client->peerUser(
			user_id : -4349923381129692765,
		),
		$client->peerChat(
			chat_id : 5079008007892805733,
		),
		$client->peerChannel(
			channel_id : 2254630357187711588,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 7749278796988739063,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -8495109636470882738,
			title : 'ino7ACGUV49OJT3E',
			photo : $client->chatPhotoEmpty(),
			participants_count : 79,
			date : 46,
			version : 66,
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
				until_date : 54,
			),
		),
		$client->chatForbidden(
			id : 4519853822543111349,
			title : 'TM5ZyAkqYfjzFO7w',
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
			id : 7716534056998188278,
			access_hash : 7273209699835895910,
			title : 'fetZ9hURQoXmMaJq',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 55,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'X1IncM3TJmUgsY7V',
					reason : 'L9a4D6xlewkQSNYP',
					text : 'qQoKGT93HzEuhbmg',
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
				until_date : 44,
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
				until_date : 79,
			),
			participants_count : 78,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 86,
			color : $client->peerColor(
				color : 63,
				background_emoji_id : 3439662451299940768,
			),
			profile_color : $client->peerColor(
				color : 80,
				background_emoji_id : 7209481567362434204,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 57,
			subscription_until_date : 30,
			bot_verification_icon : -6103090144245141163,
			send_paid_messages_stars : 6202597073521526538,
			linked_monoforum_id : 6811769233544639424,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -6656020206145146195,
			access_hash : -6609477750909771578,
			title : 'VIEY6yFkNOCHTu3W',
			until_date : 16,
		),
	),
	users : array(
		$client->userEmpty(
			id : -5626116788589011922,
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
			id : -6248882164655262258,
			access_hash : 3901117463051107279,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 84,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'NJZK9EGs7DqCkfYc',
					reason : 'eOVU8RlI6QP1gSok',
					text : 'bzYoRSIj5W3McAwd',
				),
			),
			bot_inline_placeholder : 'QzM2InjpbyXYAs0e',
			lang_code : 'zPDmkIreoJhgGs6M',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 63,
			color : $client->peerColor(
				color : 77,
				background_emoji_id : 3912387411460826903,
			),
			profile_color : $client->peerColor(
				color : 78,
				background_emoji_id : 1852519647011097164,
			),
			bot_active_users : 63,
			bot_verification_icon : 1409410194265963351,
			send_paid_messages_stars : -2485205371969660272,
		),
	),
);
```