# phone.joinAsPeers

**Description** : *A list of peers that can be used to join a group call, presenting yourself as a specific user/channel*

**Layer** : 211

```tl
phone.joinAsPeers#afe5623f peers:Vector<Peer> chats:Vector<Chat> users:Vector<User> = phone.JoinAsPeers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peers</mark> | [`Vector<Peer>`](type/Peer) | Peers |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats mentioned in the peers vector |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users mentioned in the peers vector |

---

## Type

[phone.JoinAsPeers](type/phone.JoinAsPeers)

---

## Example

```php
$phoneJoinAsPeers = $client->phone->joinAsPeers(
	peers : array(
		$client->peerUser(
			user_id : -4026472456572197099,
		),
		$client->peerChat(
			chat_id : -6063127071906403642,
		),
		$client->peerChannel(
			channel_id : 8827676301149906820,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 5761966479087147185,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 6085807580873021706,
			title : 'XbIW03eDOiAtjQMH',
			photo : $client->chatPhotoEmpty(),
			participants_count : 53,
			date : 87,
			version : 57,
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
			id : 5557173114423395144,
			title : 'iuwgG2V0eC1ny4L7',
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
			id : -3645326310462411857,
			access_hash : -8004050451608184182,
			title : 'EkbgOawiJn2Hd4ul',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 62,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'KU9z3Vg2bOhemcG6',
					reason : 'EZgx5is4GwPVf0cp',
					text : 'deM3g7AwjVpxoIZU',
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
				until_date : 30,
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
				until_date : 67,
			),
			participants_count : 83,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 69,
			color : $client->peerColor(
				color : 69,
				background_emoji_id : -2331638355000719100,
			),
			profile_color : $client->peerColor(
				color : 99,
				background_emoji_id : -705687923831318161,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 72,
			subscription_until_date : 51,
			bot_verification_icon : 1367856857724519619,
			send_paid_messages_stars : 6079464485541380725,
			linked_monoforum_id : -2196146814565823637,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 3926764941438315130,
			access_hash : 3026890040416014243,
			title : 'hLmqoDV80yYT7BsR',
			until_date : 18,
		),
	),
	users : array(
		$client->userEmpty(
			id : 7822833910594372761,
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
			id : 5370357992303053024,
			access_hash : 5075404878782289598,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 89,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Oueb0NkwFIDHxtPK',
					reason : 'RlqY3ACs51K7HvG2',
					text : 'YD3f47Fz9NBWCrau',
				),
			),
			bot_inline_placeholder : 'kdNuGsjJWMmVYcUB',
			lang_code : 'x0uzGcan6TUMqC35',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 61,
			color : $client->peerColor(
				color : 82,
				background_emoji_id : -4403630120960543887,
			),
			profile_color : $client->peerColor(
				color : 60,
				background_emoji_id : -4182606033332722498,
			),
			bot_active_users : 100,
			bot_verification_icon : 4517686894448872778,
			send_paid_messages_stars : 1038072108497757837,
		),
	),
);
```