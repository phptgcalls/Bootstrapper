# account.privacyRules

**Description** : *Privacy rules*

**Layer** : 211

```tl
account.privacyRules#50a04e45 rules:Vector<PrivacyRule> chats:Vector<Chat> users:Vector<User> = account.PrivacyRules;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>rules</mark> | [`Vector<PrivacyRule>`](type/PrivacyRule) | Privacy rules |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats to which the rules apply |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users to which the rules apply |

---

## Type

[account.PrivacyRules](type/account.PrivacyRules)

---

## Example

```php
$accountPrivacyRules = $client->account->privacyRules(
	rules : array(
		$client->privacyValueAllowContacts(),
		$client->privacyValueAllowAll(),
		$client->privacyValueAllowUsers(
			users : array(-3444915257143727092),
		),
		$client->privacyValueDisallowContacts(),
		$client->privacyValueDisallowAll(),
		$client->privacyValueDisallowUsers(
			users : array(-6213492952951810395),
		),
		$client->privacyValueAllowChatParticipants(
			chats : array(-7845071896837674411),
		),
		$client->privacyValueDisallowChatParticipants(
			chats : array(-4682249497382969282),
		),
		$client->privacyValueAllowCloseFriends(),
		$client->privacyValueAllowPremium(),
		$client->privacyValueAllowBots(),
		$client->privacyValueDisallowBots(),
	),
	chats : array(
		$client->chatEmpty(
			id : 5796775051642834242,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -2115221361521308969,
			title : 'c7HDQlmeOnukgCjP',
			photo : $client->chatPhotoEmpty(),
			participants_count : 58,
			date : 8,
			version : 14,
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
				until_date : 90,
			),
		),
		$client->chatForbidden(
			id : 8434886001046505092,
			title : 'JInvbxs3FNKqBwSi',
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
			id : 1816339281928233628,
			access_hash : 3031019163362456309,
			title : 'jKYOR3LxnHuX80AT',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 48,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '3OHFTXGvDYUaVbxZ',
					reason : '9Xc8ybhm6Ou74Flr',
					text : 'l2V81WKc6oNCL4UY',
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
				until_date : 29,
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
				until_date : 18,
			),
			participants_count : 89,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 73,
			color : $client->peerColor(
				color : 52,
				background_emoji_id : -7662041397232196583,
			),
			profile_color : $client->peerColor(
				color : 5,
				background_emoji_id : 5180138610531469892,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 71,
			subscription_until_date : 76,
			bot_verification_icon : 6998978128263693776,
			send_paid_messages_stars : 1934622891856944618,
			linked_monoforum_id : 6006265949989634282,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -6747189126886723894,
			access_hash : 6424432920355767929,
			title : 'Z3IuWalnCqsfwThY',
			until_date : 64,
		),
	),
	users : array(
		$client->userEmpty(
			id : 8726289178751259764,
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
			id : 5720078243937566839,
			access_hash : 1925674893611448204,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 21,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'BpkX4PYHAfnIW527',
					reason : 'tvcdI6rkywONlPf0',
					text : 'KR0rBWMloLeymOcQ',
				),
			),
			bot_inline_placeholder : 'cTOeX7Z93uhb8Vmt',
			lang_code : '5G1PxBC0KuzforHa',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 39,
			color : $client->peerColor(
				color : 93,
				background_emoji_id : 6968503510697811178,
			),
			profile_color : $client->peerColor(
				color : 37,
				background_emoji_id : 3151298777159754001,
			),
			bot_active_users : 78,
			bot_verification_icon : -3342639758386054946,
			send_paid_messages_stars : -2671703961208500716,
		),
	),
);
```