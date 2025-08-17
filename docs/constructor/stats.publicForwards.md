# stats.publicForwards

**Description** : *Contains info about the forwards of a story as a message to public chats and reposts by public channels*

**Layer** : 211

```tl
stats.publicForwards#93037e20 flags:# count:int forwards:Vector<PublicForward> next_offset:flags.0?string chats:Vector<Chat> users:Vector<User> = stats.PublicForwards;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of results |
| <mark>forwards</mark> | [`Vector<PublicForward>`](type/PublicForward) | Info about the forwards of a story |
| **next_offset** | [`flags.0?string`](type/string) | Offset used for pagination |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[stats.PublicForwards](type/stats.PublicForwards)

---

## Example

```php
$statsPublicForwards = $client->stats->publicForwards(
	count : 74,
	forwards : array(
		$client->publicForwardMessage(
			message : $client->messageEmpty(
				id : 33,
				peer_id : $client->peerUser(...),
			),
		),
		$client->publicForwardStory(
			peer : $client->peerUser(
				user_id : -3484025510513093755,
			),
			story : $client->storyItemDeleted(
				id : 11,
			),
		),
	),
	next_offset : 'J9sr4h8pWOBPSyja',
	chats : array(
		$client->chatEmpty(
			id : 7264121742257437594,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 3725927941691219241,
			title : 'aT6bAO0C38tiF5vz',
			photo : $client->chatPhotoEmpty(),
			participants_count : 4,
			date : 54,
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
				until_date : 76,
			),
		),
		$client->chatForbidden(
			id : -5880654522101219228,
			title : 'DSgd9RcmPHt1iTfF',
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
			id : -9079732460785299643,
			access_hash : 3982005853957791534,
			title : 'ZdKxYEA7zT2USkwt',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 63,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Oq4pojciM13REVHu',
					reason : 'nvY8xEJqR2mI1AHf',
					text : 'iSfmsTkwHRZl9LqC',
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
				until_date : 94,
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
				until_date : 78,
			),
			participants_count : 66,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 50,
			color : $client->peerColor(
				color : 0,
				background_emoji_id : -1857295646979388540,
			),
			profile_color : $client->peerColor(
				color : 63,
				background_emoji_id : -1924432022385398996,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 37,
			subscription_until_date : 89,
			bot_verification_icon : 8886165886587348525,
			send_paid_messages_stars : -989292199001359234,
			linked_monoforum_id : -6445748071905460001,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -1504437649434477356,
			access_hash : -5516603377172849607,
			title : 'tFcw406vSoOClRrn',
			until_date : 93,
		),
	),
	users : array(
		$client->userEmpty(
			id : 7615914641023640889,
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
			id : 5870712200951925779,
			access_hash : 7299690625761194999,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 14,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'oILAcpnhubQHGEJM',
					reason : 'CTUnk2NW0jqSrzl8',
					text : 'Z5cghka9K3MRHV0I',
				),
			),
			bot_inline_placeholder : 'Jh3W5btuazInTUqH',
			lang_code : 'ErzFaOwnL6DM3iWR',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 92,
			color : $client->peerColor(
				color : 32,
				background_emoji_id : -5762969391764667206,
			),
			profile_color : $client->peerColor(
				color : 29,
				background_emoji_id : -8972321607262697830,
			),
			bot_active_users : 62,
			bot_verification_icon : -6300495738952218104,
			send_paid_messages_stars : 1815374986549065999,
		),
	),
);
```