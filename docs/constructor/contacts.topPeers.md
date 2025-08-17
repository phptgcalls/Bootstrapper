# contacts.topPeers

**Description** : *Top peers*

**Layer** : 211

```tl
contacts.topPeers#70b772a8 categories:Vector<TopPeerCategoryPeers> chats:Vector<Chat> users:Vector<User> = contacts.TopPeers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>categories</mark> | [`Vector<TopPeerCategoryPeers>`](type/TopPeerCategoryPeers) | Top peers by top peer category |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users |

---

## Type

[contacts.TopPeers](type/contacts.TopPeers)

---

## Example

```php
$contactsTopPeers = $client->contacts->topPeers(
	categories : array(
		$client->topPeerCategoryPeers(
			category : $client->topPeerCategoryBotsPM(),
			count : 72,
			peers : array(
				$client->topPeer(
					peer : $client->peerUser(...),
					rating : -548015.052734375,
				),
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 7230444451716766742,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 8241962639287922799,
			title : 'wOarpsMPGXEx2qQb',
			photo : $client->chatPhotoEmpty(),
			participants_count : 3,
			date : 23,
			version : 15,
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
				until_date : 64,
			),
		),
		$client->chatForbidden(
			id : -1279289666452936722,
			title : 'C7iMXkl8ObHr1vdL',
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
			id : -7335052042761624218,
			access_hash : 6531299058030057033,
			title : 'SzcDd3HyfYg4m1rA',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 18,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'X73F21GQJ45dl0BV',
					reason : 'iDLFI2v7lXNjq3QP',
					text : 'HDGWYgThIrtpCBJu',
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
				until_date : 89,
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
				until_date : 34,
			),
			participants_count : 24,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 79,
			color : $client->peerColor(
				color : 19,
				background_emoji_id : -2717753333477108310,
			),
			profile_color : $client->peerColor(
				color : 1,
				background_emoji_id : 5122033448708588806,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 27,
			subscription_until_date : 32,
			bot_verification_icon : 4435877196000166162,
			send_paid_messages_stars : -4750261979010752506,
			linked_monoforum_id : -535267006812099887,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -3642405990148445410,
			access_hash : 4064666780222015186,
			title : 'FnT4CdmIRzwMPlvp',
			until_date : 6,
		),
	),
	users : array(
		$client->userEmpty(
			id : 5221433027915256451,
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
			id : -4293722024213857580,
			access_hash : 1841624666000088959,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 70,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'MWmn82AET4eyShrU',
					reason : 'RCVyd0lLmMO3fFgP',
					text : 'LtxPp2wvieIuX9Ur',
				),
			),
			bot_inline_placeholder : 'AyH6g8Bu0YdpTZ5I',
			lang_code : 'tHhVPj8Cb0IYlDJr',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 26,
			color : $client->peerColor(
				color : 36,
				background_emoji_id : -6088009253570176843,
			),
			profile_color : $client->peerColor(
				color : 56,
				background_emoji_id : 3507860862416983910,
			),
			bot_active_users : 91,
			bot_verification_icon : -6841078716850125706,
			send_paid_messages_stars : -3255913077724123218,
		),
	),
);
```