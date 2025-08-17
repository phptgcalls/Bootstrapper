# account.resolvedBusinessChatLinks

**Description** : *Contains info about a single resolved business chat deep link »*

**Layer** : 211

```tl
account.resolvedBusinessChatLinks#9a23af21 flags:# peer:Peer message:string entities:flags.0?Vector<MessageEntity> chats:Vector<Chat> users:Vector<User> = account.ResolvedBusinessChatLinks;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>peer</mark> | [`Peer`](type/Peer) | Destination peer |
| <mark>message</mark> | [`string`](type/string) | Message to pre-fill in the message input field |
| **entities** | [`flags.0?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[account.ResolvedBusinessChatLinks](type/account.ResolvedBusinessChatLinks)

---

## Example

```php
$accountResolvedBusinessChatLinks = $client->account->resolvedBusinessChatLinks(
	peer : $client->peerUser(
		user_id : -397993753683114522,
	),
	message : '9HsijluTgWKUz2or',
	entities : array(
		$client->messageEntityUnknown(
			offset : 88,
			length : 85,
		),
		$client->messageEntityMention(
			offset : 18,
			length : 20,
		),
		$client->messageEntityHashtag(
			offset : 6,
			length : 86,
		),
		$client->messageEntityBotCommand(
			offset : 85,
			length : 40,
		),
		$client->messageEntityUrl(
			offset : 7,
			length : 25,
		),
		$client->messageEntityEmail(
			offset : 59,
			length : 76,
		),
		$client->messageEntityBold(
			offset : 6,
			length : 81,
		),
		$client->messageEntityItalic(
			offset : 7,
			length : 28,
		),
		$client->messageEntityCode(
			offset : 3,
			length : 26,
		),
		$client->messageEntityPre(
			offset : 60,
			length : 20,
			language : '2azdFIyC7bO93XgY',
		),
		$client->messageEntityTextUrl(
			offset : 70,
			length : 55,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 92,
			length : 49,
			user_id : 8025222866675542993,
		),
		$client->inputMessageEntityMentionName(
			offset : 70,
			length : 99,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 72,
			length : 50,
		),
		$client->messageEntityCashtag(
			offset : 77,
			length : 97,
		),
		$client->messageEntityUnderline(
			offset : 69,
			length : 78,
		),
		$client->messageEntityStrike(
			offset : 7,
			length : 27,
		),
		$client->messageEntityBankCard(
			offset : 69,
			length : 88,
		),
		$client->messageEntitySpoiler(
			offset : 81,
			length : 83,
		),
		$client->messageEntityCustomEmoji(
			offset : 88,
			length : 94,
			document_id : 7599376451130890831,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 55,
			length : 72,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 9174049983000327553,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -989444357536305287,
			title : 'yd7xcQqAtHjnJYr9',
			photo : $client->chatPhotoEmpty(),
			participants_count : 63,
			date : 7,
			version : 81,
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
				until_date : 94,
			),
		),
		$client->chatForbidden(
			id : -1638466155064608168,
			title : 'k4XLNhqEn15J9WQt',
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
			id : 3700822037901818812,
			access_hash : 6962379362564395823,
			title : 'qZN3HYD7jozcpF46',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 8,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'X07BsnoR3j4S2pOG',
					reason : 'P5FDouEcmkvdTrNG',
					text : 'QE7odgTmRzwObHur',
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
				until_date : 38,
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
				until_date : 16,
			),
			participants_count : 66,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 75,
			color : $client->peerColor(
				color : 20,
				background_emoji_id : -8867504848229223292,
			),
			profile_color : $client->peerColor(
				color : 94,
				background_emoji_id : 1349680413153388937,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 76,
			subscription_until_date : 43,
			bot_verification_icon : 5776014533963037515,
			send_paid_messages_stars : -6476073424697947924,
			linked_monoforum_id : 292746157800327369,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 1910844521443255961,
			access_hash : -4692966880833500162,
			title : 'enlv5N9u6sMhAFPD',
			until_date : 43,
		),
	),
	users : array(
		$client->userEmpty(
			id : -421058582769963027,
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
			id : -7159741989395016784,
			access_hash : 6838583381277326461,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 21,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'vzbpGXYNUZVleOkc',
					reason : 'YotqzZVCFOiMWwuL',
					text : 'iaLEQrNbcTq7XRVG',
				),
			),
			bot_inline_placeholder : 'VJabHEcnG8hN7tqZ',
			lang_code : 'VHSkBfiKmaZ0EOAP',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 96,
			color : $client->peerColor(
				color : 85,
				background_emoji_id : -4235939647880055951,
			),
			profile_color : $client->peerColor(
				color : 78,
				background_emoji_id : 6923185409536956639,
			),
			bot_active_users : 52,
			bot_verification_icon : 5063407127221629109,
			send_paid_messages_stars : 3741820845226240652,
		),
	),
);
```