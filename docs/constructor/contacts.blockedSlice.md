# contacts.blockedSlice

**Description** : *Incomplete list of blocked users*

**Layer** : 211

```tl
contacts.blockedSlice#e1664194 count:int blocked:Vector<PeerBlocked> chats:Vector<Chat> users:Vector<User> = contacts.Blocked;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Total number of elements in the list |
| <mark>blocked</mark> | [`Vector<PeerBlocked>`](type/PeerBlocked) | List of blocked users |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Blocked chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of users |

---

## Type

[contacts.Blocked](type/contacts.Blocked)

---

## Example

```php
$contactsBlocked = $client->contacts->blockedSlice(
	count : 95,
	blocked : array(
		$client->peerBlocked(
			peer_id : $client->peerUser(
				user_id : -7105050741537076692,
			),
			date : 81,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -8633578478243390612,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 6196403392014500463,
			title : 'yjsKZnTFXD32HW1P',
			photo : $client->chatPhotoEmpty(),
			participants_count : 63,
			date : 11,
			version : 45,
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
			id : 6898405218039355324,
			title : '8pzfQNnmOxKJTaB1',
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
			id : -2748332583840798443,
			access_hash : -2870238622977421836,
			title : 'PMpRcKdoNB758eWs',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 69,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'CH7P3wtI1WDyEvJX',
					reason : 'hQPZFYMWsnblmERU',
					text : 'Z1lDj7z0RJmxOIrQ',
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
				until_date : 14,
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
				until_date : 39,
			),
			participants_count : 18,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 39,
			color : $client->peerColor(
				color : 88,
				background_emoji_id : -4368842944095811935,
			),
			profile_color : $client->peerColor(
				color : 81,
				background_emoji_id : 9163516560380684793,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 67,
			subscription_until_date : 77,
			bot_verification_icon : -8933634100637756909,
			send_paid_messages_stars : -2211096628312829991,
			linked_monoforum_id : 7294567438578793099,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 1898313460091860652,
			access_hash : 3476363766527492025,
			title : 'tfInR6ivqEJ3LZs5',
			until_date : 41,
		),
	),
	users : array(
		$client->userEmpty(
			id : -4330222553590219089,
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
			id : -6652609967793468536,
			access_hash : 1566277114854575955,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 3,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'gJcp4bEufr7Aseaq',
					reason : '0QIkKnbuNVPSELAC',
					text : 'VIPuifqbEJlx3cD7',
				),
			),
			bot_inline_placeholder : 'KJyrPCDwGEs5ex32',
			lang_code : 'NjO7aQcsFwZDp9Xv',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 93,
			color : $client->peerColor(
				color : 62,
				background_emoji_id : -3714942972520101973,
			),
			profile_color : $client->peerColor(
				color : 54,
				background_emoji_id : 6046846030505604944,
			),
			bot_active_users : 34,
			bot_verification_icon : 6658901647074364761,
			send_paid_messages_stars : -5990704998660661498,
		),
	),
);
```