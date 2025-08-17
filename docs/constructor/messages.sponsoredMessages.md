# messages.sponsoredMessages

**Description** : *A set of sponsored messages associated to a channel*

**Layer** : 211

```tl
messages.sponsoredMessages#ffda656d flags:# posts_between:flags.0?int start_delay:flags.1?int between_delay:flags.2?int messages:Vector<SponsoredMessage> chats:Vector<Chat> users:Vector<User> = messages.SponsoredMessages;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **posts_between** | [`flags.0?int`](type/int) | If set, specifies the minimum number of messages between shown sponsored messages; otherwise, only one sponsored message must be shown after all ordinary messages |
| **start_delay** | [`flags.1?int`](type/int) | NOTHING |
| **between_delay** | [`flags.2?int`](type/int) | NOTHING |
| <mark>messages</mark> | [`Vector<SponsoredMessage>`](type/SponsoredMessage) | Sponsored messages |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats mentioned in the sponsored messages |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users mentioned in the sponsored messages |

---

## Type

[messages.SponsoredMessages](type/messages.SponsoredMessages)

---

## Example

```php
$messagesSponsoredMessages = $client->messages->sponsoredMessages(
	posts_between : 34,
	start_delay : 18,
	between_delay : 44,
	messages : array(
		$client->sponsoredMessage(
			recommended : true,
			can_report : true,
			random_id : 'ɤ?5?LiveProto?ʚj`',
			url : 'https://docs.liveproto.dev',
			title : 'T9rnlYeHkKFL3hVJ',
			message : '3dtIh8HGycqfrARV',
			entities : array(
				$client->messageEntityUnknown(
					offset : 8,
					length : 6,
				),
				$client->messageEntityMention(
					offset : 50,
					length : 80,
				),
				$client->messageEntityHashtag(
					offset : 9,
					length : 13,
				),
				$client->messageEntityBotCommand(
					offset : 94,
					length : 92,
				),
				$client->messageEntityUrl(
					offset : 37,
					length : 43,
				),
				$client->messageEntityEmail(
					offset : 59,
					length : 66,
				),
				$client->messageEntityBold(
					offset : 65,
					length : 53,
				),
				$client->messageEntityItalic(
					offset : 72,
					length : 13,
				),
				$client->messageEntityCode(
					offset : 61,
					length : 73,
				),
				$client->messageEntityPre(
					offset : 2,
					length : 72,
					language : '7xY0moR8Sl1hgEP9',
				),
				$client->messageEntityTextUrl(
					offset : 68,
					length : 26,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 15,
					length : 53,
					user_id : -3407262941423739617,
				),
				$client->inputMessageEntityMentionName(
					offset : 34,
					length : 92,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 69,
					length : 80,
				),
				$client->messageEntityCashtag(
					offset : 25,
					length : 57,
				),
				$client->messageEntityUnderline(
					offset : 15,
					length : 27,
				),
				$client->messageEntityStrike(
					offset : 88,
					length : 89,
				),
				$client->messageEntityBankCard(
					offset : 87,
					length : 53,
				),
				$client->messageEntitySpoiler(
					offset : 62,
					length : 39,
				),
				$client->messageEntityCustomEmoji(
					offset : 5,
					length : 90,
					document_id : -5344878113337448673,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 32,
					length : 99,
				),
			),
			photo : $client->photoEmpty(
				id : 8440633688277869513,
			),
			media : $client->messageMediaEmpty(),
			color : $client->peerColor(
				color : 63,
				background_emoji_id : -6436577316159098677,
			),
			button_text : 'ycCBxtS7zRQ8fLGk',
			sponsor_info : '3jFpI4Mgl2iW7oJT',
			additional_info : 'QdEF8g2TenDOlzh7',
			min_display_duration : 44,
			max_display_duration : 86,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 6348309134422409305,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 1877554597832532690,
			title : 'oQd679jhpTlPCexJ',
			photo : $client->chatPhotoEmpty(),
			participants_count : 74,
			date : 17,
			version : 73,
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
				until_date : 98,
			),
		),
		$client->chatForbidden(
			id : 5558321021730240754,
			title : '6WCzNDhcoy41mLjx',
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
			id : 5745458734539003307,
			access_hash : -1395342403393688628,
			title : 'tmKC7AxwbI9PgGVN',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 10,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Lbt7MEaleGOQ25ND',
					reason : 'aJFG5mf2Ig8hKbzc',
					text : '35DjeQUxXw7tTkVu',
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
				until_date : 25,
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
				until_date : 43,
			),
			participants_count : 32,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 75,
			color : $client->peerColor(
				color : 5,
				background_emoji_id : -23175179596910764,
			),
			profile_color : $client->peerColor(
				color : 70,
				background_emoji_id : 861702087085472415,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 5,
			subscription_until_date : 88,
			bot_verification_icon : -8260917626607916858,
			send_paid_messages_stars : -160595041641159875,
			linked_monoforum_id : 2954589848062148318,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 7833783916324710232,
			access_hash : -8644621185493354730,
			title : 'aPbs4eFDT6pu9czw',
			until_date : 58,
		),
	),
	users : array(
		$client->userEmpty(
			id : -8036196798631606514,
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
			id : 8175690746787799167,
			access_hash : -4943180430315892888,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 87,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'ym49Z2jMp1i7YSgA',
					reason : 'knNd1zmUWlhjL3qE',
					text : 'QXtBCHR9ma2EKcDP',
				),
			),
			bot_inline_placeholder : 'uUalmcQK1bNoRSxH',
			lang_code : 'ERf9suwna47vLh8F',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 33,
			color : $client->peerColor(
				color : 78,
				background_emoji_id : -4570228113992958055,
			),
			profile_color : $client->peerColor(
				color : 76,
				background_emoji_id : 3158192587387440852,
			),
			bot_active_users : 93,
			bot_verification_icon : -7804815517026097166,
			send_paid_messages_stars : 5343955369297640018,
		),
	),
);
```