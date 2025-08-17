# chatlists.chatlistInvite

**Description** : *Info about a chat folder deep link »*

**Layer** : 211

```tl
chatlists.chatlistInvite#f10ece2f flags:# title_noanimate:flags.1?true title:TextWithEntities emoticon:flags.0?string peers:Vector<Peer> chats:Vector<Chat> users:Vector<User> = chatlists.ChatlistInvite;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **title_noanimate** | [`flags.1?true`](type/true) | NOTHING |
| <mark>title</mark> | [`TextWithEntities`](type/TextWithEntities) | Name of the link |
| **emoticon** | [`flags.0?string`](type/string) | Emoji to use as icon for the folder |
| <mark>peers</mark> | [`Vector<Peer>`](type/Peer) | Supergroups and channels to join |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Related chat information |
| <mark>users</mark> | [`Vector<User>`](type/User) | Related user information |

---

## Type

[chatlists.ChatlistInvite](type/chatlists.ChatlistInvite)

---

## Example

```php
$chatlistsChatlistInvite = $client->chatlists->chatlistInvite(
	title_noanimate : true,
	title : $client->textWithEntities(
		text : '4REaJYvtjBurkoIs',
		entities : array(
			$client->messageEntityUnknown(
				offset : 60,
				length : 95,
			),
			$client->messageEntityMention(
				offset : 45,
				length : 9,
			),
			$client->messageEntityHashtag(
				offset : 3,
				length : 98,
			),
			$client->messageEntityBotCommand(
				offset : 15,
				length : 49,
			),
			$client->messageEntityUrl(
				offset : 23,
				length : 11,
			),
			$client->messageEntityEmail(
				offset : 72,
				length : 91,
			),
			$client->messageEntityBold(
				offset : 25,
				length : 49,
			),
			$client->messageEntityItalic(
				offset : 86,
				length : 29,
			),
			$client->messageEntityCode(
				offset : 19,
				length : 59,
			),
			$client->messageEntityPre(
				offset : 4,
				length : 64,
				language : 'gh4b1JVjcxyqv9IN',
			),
			$client->messageEntityTextUrl(
				offset : 89,
				length : 22,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 54,
				length : 52,
				user_id : -4036524511719960596,
			),
			$client->inputMessageEntityMentionName(
				offset : 67,
				length : 92,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 82,
				length : 93,
			),
			$client->messageEntityCashtag(
				offset : 76,
				length : 27,
			),
			$client->messageEntityUnderline(
				offset : 42,
				length : 32,
			),
			$client->messageEntityStrike(
				offset : 26,
				length : 55,
			),
			$client->messageEntityBankCard(
				offset : 53,
				length : 23,
			),
			$client->messageEntitySpoiler(
				offset : 87,
				length : 96,
			),
			$client->messageEntityCustomEmoji(
				offset : 72,
				length : 55,
				document_id : -4291623331816000949,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 7,
				length : 17,
			),
		),
	),
	emoticon : 'O3eDAC8aKbl5xc14',
	peers : array(
		$client->peerUser(
			user_id : -3429315501034672200,
		),
		$client->peerChat(
			chat_id : -8020362004812107897,
		),
		$client->peerChannel(
			channel_id : -1258697097052955258,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -5052241671579555853,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 4698575098942188102,
			title : 'AP4wuXybfSKz0UD2',
			photo : $client->chatPhotoEmpty(),
			participants_count : 45,
			date : 88,
			version : 1,
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
				until_date : 29,
			),
		),
		$client->chatForbidden(
			id : -9192846952151729485,
			title : 'x1yG9ifN5YV0pIDd',
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
			id : -4258318918125513341,
			access_hash : 5629134032406926783,
			title : 'Y7Namly3SQvne4jo',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 75,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'aWv027meiYcCud59',
					reason : 'h4UoLCqbNpZvQYxf',
					text : 'FJ7XkPtGgobYhDCp',
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
				until_date : 72,
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
				until_date : 57,
			),
			participants_count : 27,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 23,
			color : $client->peerColor(
				color : 51,
				background_emoji_id : -5606478596697078132,
			),
			profile_color : $client->peerColor(
				color : 88,
				background_emoji_id : 1037019909868227447,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 29,
			subscription_until_date : 52,
			bot_verification_icon : 8440725201000102096,
			send_paid_messages_stars : -4459198197279486221,
			linked_monoforum_id : -6089836359971235908,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 1653837081142905275,
			access_hash : 3202306676144684437,
			title : 'dD9pn8Tote25QzFO',
			until_date : 57,
		),
	),
	users : array(
		$client->userEmpty(
			id : 3691965506235675545,
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
			id : -5459649843961331770,
			access_hash : 1686738016631433212,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 18,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'H9ygOaXsqnLRkAhd',
					reason : '89qtiGBTpJ0YAdXu',
					text : 'BcZUu3Rqgx2TMnlp',
				),
			),
			bot_inline_placeholder : 'dEfX7r1sUBqlzh0p',
			lang_code : 'fGrmWI145qdybO7n',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 85,
			color : $client->peerColor(
				color : 32,
				background_emoji_id : 8484430720025558537,
			),
			profile_color : $client->peerColor(
				color : 54,
				background_emoji_id : -3442234473839915468,
			),
			bot_active_users : 74,
			bot_verification_icon : 4835999134891914358,
			send_paid_messages_stars : 5069409649562229000,
		),
	),
);
```