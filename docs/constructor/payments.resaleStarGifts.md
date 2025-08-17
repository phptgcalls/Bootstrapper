# payments.resaleStarGifts

**Layer** : 211

```tl
payments.resaleStarGifts#947a12df flags:# count:int gifts:Vector<StarGift> next_offset:flags.0?string attributes:flags.1?Vector<StarGiftAttribute> attributes_hash:flags.1?long chats:Vector<Chat> counters:flags.2?Vector<StarGiftAttributeCounter> users:Vector<User> = payments.ResaleStarGifts;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| <mark>count</mark> | [`int`](type/int) | NOTHING |
| <mark>gifts</mark> | [`Vector<StarGift>`](type/StarGift) | NOTHING |
| **next_offset** | [`flags.0?string`](type/string) | NOTHING |
| **attributes** | [`flags.1?Vector<StarGiftAttribute>`](type/StarGiftAttribute) | NOTHING |
| **attributes_hash** | [`flags.1?long`](type/long) | NOTHING |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | NOTHING |
| **counters** | [`flags.2?Vector<StarGiftAttributeCounter>`](type/StarGiftAttributeCounter) | NOTHING |
| <mark>users</mark> | [`Vector<User>`](type/User) | NOTHING |

---

## Type

[payments.ResaleStarGifts](type/payments.ResaleStarGifts)

---

## Example

```php
$paymentsResaleStarGifts = $client->payments->resaleStarGifts(
	count : 4,
	gifts : array(
		$client->starGift(
			limited : true,
			sold_out : true,
			birthday : true,
			require_premium : true,
			limited_per_user : true,
			id : -2330542898559027672,
			sticker : $client->documentEmpty(
				id : 6892049815027375658,
			),
			stars : -7922475374513366567,
			availability_remains : 53,
			availability_total : 2,
			availability_resale : -4464512042662670006,
			convert_stars : 4584062766181467631,
			first_sale_date : 66,
			last_sale_date : 91,
			upgrade_stars : -1872907239933767770,
			resell_min_stars : 8664969784783898533,
			title : 'NmZVcOiUFzvTdoeR',
			released_by : $client->peerUser(
				user_id : -2139545142361871057,
			),
			per_user_total : 55,
			per_user_remains : 18,
		),
		$client->starGiftUnique(
			require_premium : true,
			resale_ton_only : true,
			id : -558192117720344807,
			title : 'p1le7XE2HLK5RQAW',
			slug : '0wY8Jbrlqjvuta7c',
			num : 43,
			owner_id : $client->peerUser(
				user_id : 1529889653163892631,
			),
			owner_name : 'wUgZfdhy5cRDemBV',
			owner_address : 'soyeK67N0jGzv4c2',
			attributes : array(
				$client->starGiftAttributeModel(
					name : 'R4FvAMnEYqkGz5SL',
					document : $client->documentEmpty(...),
					rarity_permille : 77,
				),
				$client->starGiftAttributePattern(
					name : 'qMdpvlfrcRX7IL6m',
					document : $client->documentEmpty(...),
					rarity_permille : 78,
				),
				$client->starGiftAttributeBackdrop(
					name : 'rW5DxpFoLzhnH9l1',
					backdrop_id : 32,
					center_color : 97,
					edge_color : 87,
					pattern_color : 80,
					text_color : 18,
					rarity_permille : 67,
				),
				$client->starGiftAttributeOriginalDetails(
					sender_id : $client->peerUser(...),
					recipient_id : $client->peerUser(...),
					date : 82,
					message : $client->textWithEntities(...),
				),
			),
			availability_issued : 19,
			availability_total : 91,
			gift_address : 'Wwi2O0JljyG4sSQv',
			resell_amount : array(
				$client->starsAmount(
					amount : 8513904455513334185,
					nanos : 14,
				),
				$client->starsTonAmount(
					amount : -8917004435774814260,
				),
			),
			released_by : $client->peerUser(
				user_id : 3457209882149857640,
			),
		),
	),
	next_offset : '3CsbMNyczZ4ErqDS',
	attributes : array(
		$client->starGiftAttributeModel(
			name : 'wP5XQLjepJS92WmU',
			document : $client->documentEmpty(
				id : -348971863148780784,
			),
			rarity_permille : 26,
		),
		$client->starGiftAttributePattern(
			name : '4Tz7P1Z0JotVGkSj',
			document : $client->documentEmpty(
				id : 3329522930663385625,
			),
			rarity_permille : 1,
		),
		$client->starGiftAttributeBackdrop(
			name : 'LQAlnmV8pPi9YHuf',
			backdrop_id : 57,
			center_color : 11,
			edge_color : 88,
			pattern_color : 25,
			text_color : 7,
			rarity_permille : 70,
		),
		$client->starGiftAttributeOriginalDetails(
			sender_id : $client->peerUser(
				user_id : -3816158728708870890,
			),
			recipient_id : $client->peerUser(
				user_id : -9056300111776700017,
			),
			date : 57,
			message : $client->textWithEntities(
				text : 'lDWCmYAjN5GXFJPs',
				entities : array(
					$client->messageEntityUnknown(...),
					$client->messageEntityMention(...),
					$client->messageEntityHashtag(...),
					$client->messageEntityBotCommand(...),
					$client->messageEntityUrl(...),
					$client->messageEntityEmail(...),
					$client->messageEntityBold(...),
					$client->messageEntityItalic(...),
					$client->messageEntityCode(...),
					$client->messageEntityPre(...),
					$client->messageEntityTextUrl(...),
					$client->messageEntityMentionName(...),
					$client->inputMessageEntityMentionName(...),
					$client->messageEntityPhone(...),
					$client->messageEntityCashtag(...),
					$client->messageEntityUnderline(...),
					$client->messageEntityStrike(...),
					$client->messageEntityBankCard(...),
					$client->messageEntitySpoiler(...),
					$client->messageEntityCustomEmoji(...),
					$client->messageEntityBlockquote(...),
				),
			),
		),
	),
	attributes_hash : 1884800091867865598,
	chats : array(
		$client->chatEmpty(
			id : -2045302406814188628,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 2533188576247827310,
			title : 'C0sBQyjFwaMdqRpr',
			photo : $client->chatPhotoEmpty(),
			participants_count : 39,
			date : 33,
			version : 29,
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
				until_date : 51,
			),
		),
		$client->chatForbidden(
			id : -8191368436969646253,
			title : 'VXr8OjnSJIzqhAH9',
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
			id : -8985158109318546046,
			access_hash : -2608551555973038579,
			title : 'j5A7EZ0La8dpThVu',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 46,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '3yXHRsdDI0P9zSge',
					reason : 'vZfJ9ObydE57YD0X',
					text : 'DYBEf7UgydMqjati',
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
				until_date : 23,
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
				until_date : 48,
			),
			participants_count : 81,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 17,
			color : $client->peerColor(
				color : 93,
				background_emoji_id : -3547174467356403610,
			),
			profile_color : $client->peerColor(
				color : 65,
				background_emoji_id : -7560422910670767138,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 77,
			subscription_until_date : 89,
			bot_verification_icon : 6858076347384291886,
			send_paid_messages_stars : -3977574804686871049,
			linked_monoforum_id : -5867254948765328323,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 3901372053356096490,
			access_hash : -903287888272351670,
			title : 'jwohHLS8WI2ticNa',
			until_date : 58,
		),
	),
	counters : array(
		$client->starGiftAttributeCounter(
			attribute : $client->starGiftAttributeIdModel(
				document_id : 2602620556768704445,
			),
			count : 98,
		),
	),
	users : array(
		$client->userEmpty(
			id : -3985028747763844358,
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
			id : -2176531399576345240,
			access_hash : -4608023641724041100,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 42,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '6WTCrAg9E78fk3IO',
					reason : 'MdZ510wPEmVTLWQX',
					text : 'WiUZ9EcLthJQRvxu',
				),
			),
			bot_inline_placeholder : 'VbpQf0Cxn9j82HqD',
			lang_code : 'i8eYuNmMgVnvoTcl',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 98,
			color : $client->peerColor(
				color : 65,
				background_emoji_id : -5655078556013011084,
			),
			profile_color : $client->peerColor(
				color : 40,
				background_emoji_id : 2839518765254786611,
			),
			bot_active_users : 94,
			bot_verification_icon : 8362542746957065746,
			send_paid_messages_stars : 7767345537810908290,
		),
	),
);
```