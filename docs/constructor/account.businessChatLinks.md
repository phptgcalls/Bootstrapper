# account.businessChatLinks

**Description** : *Contains info about business chat deep links » created by the current account*

**Layer** : 211

```tl
account.businessChatLinks#ec43a2d1 links:Vector<BusinessChatLink> chats:Vector<Chat> users:Vector<User> = account.BusinessChatLinks;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>links</mark> | [`Vector<BusinessChatLink>`](type/BusinessChatLink) | Links |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[account.BusinessChatLinks](type/account.BusinessChatLinks)

---

## Example

```php
$accountBusinessChatLinks = $client->account->businessChatLinks(
	links : array(
		$client->businessChatLink(
			link : 'V39riZz2sUYcuqBK',
			message : 'SDdY1KLGE3armPts',
			entities : array(
				$client->messageEntityUnknown(
					offset : 65,
					length : 51,
				),
				$client->messageEntityMention(
					offset : 84,
					length : 61,
				),
				$client->messageEntityHashtag(
					offset : 31,
					length : 85,
				),
				$client->messageEntityBotCommand(
					offset : 35,
					length : 48,
				),
				$client->messageEntityUrl(
					offset : 29,
					length : 16,
				),
				$client->messageEntityEmail(
					offset : 38,
					length : 71,
				),
				$client->messageEntityBold(
					offset : 60,
					length : 19,
				),
				$client->messageEntityItalic(
					offset : 82,
					length : 84,
				),
				$client->messageEntityCode(
					offset : 62,
					length : 63,
				),
				$client->messageEntityPre(
					offset : 58,
					length : 34,
					language : 'wfazerWZCvOXGhR4',
				),
				$client->messageEntityTextUrl(
					offset : 60,
					length : 13,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 67,
					length : 92,
					user_id : 3477762007979899311,
				),
				$client->inputMessageEntityMentionName(
					offset : 35,
					length : 87,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 77,
					length : 49,
				),
				$client->messageEntityCashtag(
					offset : 43,
					length : 87,
				),
				$client->messageEntityUnderline(
					offset : 87,
					length : 99,
				),
				$client->messageEntityStrike(
					offset : 66,
					length : 30,
				),
				$client->messageEntityBankCard(
					offset : 44,
					length : 80,
				),
				$client->messageEntitySpoiler(
					offset : 13,
					length : 9,
				),
				$client->messageEntityCustomEmoji(
					offset : 67,
					length : 57,
					document_id : 4053512811334891786,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 70,
					length : 30,
				),
			),
			title : 'Kzf9owAnLYjdgMmW',
			views : 65,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 93196856715770010,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 3727113229614321638,
			title : 'uVOayozPtB7WGqQA',
			photo : $client->chatPhotoEmpty(),
			participants_count : 64,
			date : 91,
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
				until_date : 80,
			),
		),
		$client->chatForbidden(
			id : 1534706796063267970,
			title : 'jOgIcfNdX7avm4Ql',
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
			id : 3811054450813361797,
			access_hash : -560342442707200762,
			title : 'PQiKBq9mfoGpdgHy',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 26,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'kZDTErPWGa9iYt7c',
					reason : 'w0SdsG9FDI5yU8AO',
					text : 'X1atWrg5UGZkm4BQ',
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
				until_date : 71,
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
			participants_count : 18,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 92,
			color : $client->peerColor(
				color : 82,
				background_emoji_id : -8979074031894167766,
			),
			profile_color : $client->peerColor(
				color : 66,
				background_emoji_id : 4237811090504479751,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 66,
			subscription_until_date : 40,
			bot_verification_icon : 389802132871752995,
			send_paid_messages_stars : -6687286208727098564,
			linked_monoforum_id : -6381641289240382009,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 7917769642938930846,
			access_hash : 1727222092841304981,
			title : 'S4LU8kmvQljtDyXn',
			until_date : 77,
		),
	),
	users : array(
		$client->userEmpty(
			id : 5417783794408592581,
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
			id : -1428849939892872289,
			access_hash : -5178108284031818028,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 90,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '1ZTKskEfAi4b3uYN',
					reason : 'LbT3ID92ZPOdE4qx',
					text : 'RZcoNrhESvz9J5u3',
				),
			),
			bot_inline_placeholder : 'fBcHjA6kovLEOit3',
			lang_code : '9LmYQFDIj2yvdxNR',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 88,
			color : $client->peerColor(
				color : 15,
				background_emoji_id : 8552104948991388459,
			),
			profile_color : $client->peerColor(
				color : 5,
				background_emoji_id : -9137376485329641457,
			),
			bot_active_users : 48,
			bot_verification_icon : -102269651753519319,
			send_paid_messages_stars : -7601944310145274537,
		),
	),
);
```