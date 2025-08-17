# userFull

**Description** : *Extended user info*

**Layer** : 211

```tl
userFull#7e63ce1f flags:# blocked:flags.0?true phone_calls_available:flags.4?true phone_calls_private:flags.5?true can_pin_message:flags.7?true has_scheduled:flags.12?true video_calls_available:flags.13?true voice_messages_forbidden:flags.20?true translations_disabled:flags.23?true stories_pinned_available:flags.26?true blocked_my_stories_from:flags.27?true wallpaper_overridden:flags.28?true contact_require_premium:flags.29?true read_dates_private:flags.30?true flags2:# sponsored_enabled:flags2.7?true can_view_revenue:flags2.9?true bot_can_manage_emoji_status:flags2.10?true display_gifts_button:flags2.16?true id:long about:flags.1?string settings:PeerSettings personal_photo:flags.21?Photo profile_photo:flags.2?Photo fallback_photo:flags.22?Photo notify_settings:PeerNotifySettings bot_info:flags.3?BotInfo pinned_msg_id:flags.6?int common_chats_count:int folder_id:flags.11?int ttl_period:flags.14?int theme_emoticon:flags.15?string private_forward_name:flags.16?string bot_group_admin_rights:flags.17?ChatAdminRights bot_broadcast_admin_rights:flags.18?ChatAdminRights wallpaper:flags.24?WallPaper stories:flags.25?PeerStories business_work_hours:flags2.0?BusinessWorkHours business_location:flags2.1?BusinessLocation business_greeting_message:flags2.2?BusinessGreetingMessage business_away_message:flags2.3?BusinessAwayMessage business_intro:flags2.4?BusinessIntro birthday:flags2.5?Birthday personal_channel_id:flags2.6?long personal_channel_message:flags2.6?int stargifts_count:flags2.8?int starref_program:flags2.11?StarRefProgram bot_verification:flags2.12?BotVerification send_paid_messages_stars:flags2.14?long disallowed_gifts:flags2.15?DisallowedGiftsSettings stars_rating:flags2.17?StarsRating stars_my_pending_rating:flags2.18?StarsRating stars_my_pending_rating_date:flags2.18?int = UserFull;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **blocked** | [`flags.0?true`](type/true) | Whether you have blocked this user |
| **phone_calls_available** | [`flags.4?true`](type/true) | Whether this user can make VoIP calls |
| **phone_calls_private** | [`flags.5?true`](type/true) | Whether this user's privacy settings allow you to call them |
| **can_pin_message** | [`flags.7?true`](type/true) | Whether you can pin messages in the chat with this user, you can do this only for a chat with yourself |
| **has_scheduled** | [`flags.12?true`](type/true) | Whether scheduled messages are available |
| **video_calls_available** | [`flags.13?true`](type/true) | Whether the user can receive video calls |
| **voice_messages_forbidden** | [`flags.20?true`](type/true) | Whether this user doesn't allow sending voice messages in a private chat with them |
| **translations_disabled** | [`flags.23?true`](type/true) | Whether the real-time chat translation popup should be hidden |
| **stories_pinned_available** | [`flags.26?true`](type/true) | Whether this user has some pinned stories |
| **blocked_my_stories_from** | [`flags.27?true`](type/true) | Whether we've blocked this user, preventing them from seeing our stories » |
| **wallpaper_overridden** | [`flags.28?true`](type/true) | Whether the other user has chosen a custom wallpaper for us using messages.setChatWallPaper and the for_both flag, see here » for more info |
| **contact_require_premium** | [`flags.29?true`](type/true) | If set, we cannot write to this user: subscribe to Telegram Premium to get permission to write to this user. To set this flag for ourselves invoke account.setGlobalPrivacySettings, setting the settings.new_noncontact_peers_require_premium flag, see here » for more info |
| **read_dates_private** | [`flags.30?true`](type/true) | If set, we cannot fetch the exact read date of messages we send to this user using messages.getOutboxReadDate.  The exact read date of messages might still be unavailable for other reasons, see here » for more info.  To set this flag for ourselves invoke account.setGlobalPrivacySettings, setting the settings.hide_read_marks flag |
| <mark>flags2</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **sponsored_enabled** | [`flags2.7?true`](type/true) | Whether ads were re-enabled for the current account (only accessible to the currently logged-in user), see here » for more info |
| **can_view_revenue** | [`flags2.9?true`](type/true) | If set, this user can view ad revenue statistics » for this bot |
| **bot_can_manage_emoji_status** | [`flags2.10?true`](type/true) | If set, this is a bot that can change our emoji status » |
| **display_gifts_button** | [`flags2.16?true`](type/true) | NOTHING |
| <mark>id</mark> | [`long`](type/long) | User ID |
| **about** | [`flags.1?string`](type/string) | Bio of the user |
| <mark>settings</mark> | [`PeerSettings`](type/PeerSettings) | Peer settings |
| **personal_photo** | [`flags.21?Photo`](type/Photo) | Personal profile photo, to be shown instead of profile_photo |
| **profile_photo** | [`flags.2?Photo`](type/Photo) | Profile photo |
| **fallback_photo** | [`flags.22?Photo`](type/Photo) | Fallback profile photo, displayed if no photo is present in profile_photo or personal_photo, due to privacy settings |
| <mark>notify_settings</mark> | [`PeerNotifySettings`](type/PeerNotifySettings) | Notification settings |
| **bot_info** | [`flags.3?BotInfo`](type/BotInfo) | For bots, info about the bot (bot commands, etc) |
| **pinned_msg_id** | [`flags.6?int`](type/int) | Message ID of the last pinned message |
| <mark>common_chats_count</mark> | [`int`](type/int) | Chats in common with this user |
| **folder_id** | [`flags.11?int`](type/int) | Peer folder ID, for more info click here |
| **ttl_period** | [`flags.14?int`](type/int) | Time To Live of all messages in this chat; once a message is this many seconds old, it must be deleted |
| **theme_emoticon** | [`flags.15?string`](type/string) | Emoji associated with chat theme |
| **private_forward_name** | [`flags.16?string`](type/string) | Anonymized text to be shown instead of the user's name on forwarded messages |
| **bot_group_admin_rights** | [`flags.17?ChatAdminRights`](type/ChatAdminRights) | A suggested set of administrator rights for the bot, to be shown when adding the bot as admin to a group, see here for more info on how to handle them » |
| **bot_broadcast_admin_rights** | [`flags.18?ChatAdminRights`](type/ChatAdminRights) | A suggested set of administrator rights for the bot, to be shown when adding the bot as admin to a channel, see here for more info on how to handle them » |
| **wallpaper** | [`flags.24?WallPaper`](type/WallPaper) | Wallpaper to use in the private chat with the user |
| **stories** | [`flags.25?PeerStories`](type/PeerStories) | Active stories » |
| **business_work_hours** | [`flags2.0?BusinessWorkHours`](type/BusinessWorkHours) | Telegram Business working hours » |
| **business_location** | [`flags2.1?BusinessLocation`](type/BusinessLocation) | Telegram Business location » |
| **business_greeting_message** | [`flags2.2?BusinessGreetingMessage`](type/BusinessGreetingMessage) | Telegram Business greeting message » |
| **business_away_message** | [`flags2.3?BusinessAwayMessage`](type/BusinessAwayMessage) | Telegram Business away message » |
| **business_intro** | [`flags2.4?BusinessIntro`](type/BusinessIntro) | Specifies a custom Telegram Business profile introduction » |
| **birthday** | [`flags2.5?Birthday`](type/Birthday) | Contains info about the user's birthday » |
| **personal_channel_id** | [`flags2.6?long`](type/long) | ID of the associated personal channel », that should be shown in the profile page |
| **personal_channel_message** | [`flags2.6?int`](type/int) | ID of the latest message of the associated personal channel », that should be previewed in the profile page |
| **stargifts_count** | [`flags2.8?int`](type/int) | Number of gifts the user has chosen to display on their profile |
| **starref_program** | [`flags2.11?StarRefProgram`](type/StarRefProgram) | This bot has an active referral program » |
| **bot_verification** | [`flags2.12?BotVerification`](type/BotVerification) | NOTHING |
| **send_paid_messages_stars** | [`flags2.14?long`](type/long) | NOTHING |
| **disallowed_gifts** | [`flags2.15?DisallowedGiftsSettings`](type/DisallowedGiftsSettings) | NOTHING |
| **stars_rating** | [`flags2.17?StarsRating`](type/StarsRating) | NOTHING |
| **stars_my_pending_rating** | [`flags2.18?StarsRating`](type/StarsRating) | NOTHING |
| **stars_my_pending_rating_date** | [`flags2.18?int`](type/int) | NOTHING |

---

## Type

[UserFull](type/UserFull)

---

## Example

```php
$userFull = $client->userFull(
	blocked : true,
	phone_calls_available : true,
	phone_calls_private : true,
	can_pin_message : true,
	has_scheduled : true,
	video_calls_available : true,
	voice_messages_forbidden : true,
	translations_disabled : true,
	stories_pinned_available : true,
	blocked_my_stories_from : true,
	wallpaper_overridden : true,
	contact_require_premium : true,
	read_dates_private : true,
	sponsored_enabled : true,
	can_view_revenue : true,
	bot_can_manage_emoji_status : true,
	display_gifts_button : true,
	id : 1123491001374351971,
	about : 'BV7pZOktcWITfolM',
	settings : $client->peerSettings(
		report_spam : true,
		add_contact : true,
		block_contact : true,
		share_contact : true,
		need_contacts_exception : true,
		report_geo : true,
		autoarchived : true,
		invite_members : true,
		request_chat_broadcast : true,
		business_bot_paused : true,
		business_bot_can_reply : true,
		geo_distance : 36,
		request_chat_title : 'ohH2AO08VusDgEFr',
		request_chat_date : 66,
		business_bot_id : 1925511426085092985,
		business_bot_manage_url : 'https://docs.liveproto.dev',
		charge_paid_message_stars : 764175204645404607,
		registration_month : 'cXlrEYR8qgO6ujnB',
		phone_country : '+1234567890',
		name_change_date : 57,
		photo_change_date : 79,
	),
	personal_photo : $client->photoEmpty(
		id : 3223280798543730970,
	),
	profile_photo : $client->photoEmpty(
		id : 942890582574162508,
	),
	fallback_photo : $client->photoEmpty(
		id : 6433100479704953622,
	),
	notify_settings : $client->peerNotifySettings(
		show_previews : $client->boolFalse(),
		silent : $client->boolFalse(),
		mute_until : 28,
		ios_sound : $client->notificationSoundDefault(),
		android_sound : $client->notificationSoundDefault(),
		other_sound : $client->notificationSoundDefault(),
		stories_muted : $client->boolFalse(),
		stories_hide_sender : $client->boolFalse(),
		stories_ios_sound : $client->notificationSoundDefault(),
		stories_android_sound : $client->notificationSoundDefault(),
		stories_other_sound : $client->notificationSoundDefault(),
	),
	bot_info : $client->botInfo(
		has_preview_medias : true,
		user_id : -6686207559078944981,
		description : 'fVYJRDjvE7gUq0aT',
		description_photo : $client->photoEmpty(
			id : -8411911345485350133,
		),
		description_document : $client->documentEmpty(
			id : -2241617409901719040,
		),
		commands : array(
			$client->botCommand(
				command : 'K4IkmUJwWPNqgV6b',
				description : 'fuHWiAlsCIXOGN4J',
			),
		),
		menu_button : $client->botMenuButtonDefault(),
		privacy_policy_url : 'https://docs.liveproto.dev',
		app_settings : $client->botAppSettings(
			placeholder_path : '??}?LiveProto??',
			background_color : 41,
			background_dark_color : 88,
			header_color : 82,
			header_dark_color : 28,
		),
		verifier_settings : $client->botVerifierSettings(
			can_modify_custom_description : true,
			icon : -6127150033903321947,
			company : 'aQZDngB4eqybY2rV',
			custom_description : 'iR85M6GvKZAh3NPE',
		),
	),
	pinned_msg_id : 80,
	common_chats_count : 74,
	folder_id : 17,
	ttl_period : 92,
	theme_emoticon : 'glYcnfMeVJbBdrU9',
	private_forward_name : 'bngXJKOE6jGUxrYR',
	bot_group_admin_rights : $client->chatAdminRights(
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
	bot_broadcast_admin_rights : $client->chatAdminRights(
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
	wallpaper : $client->wallPaper(
		id : 6730444728495149096,
		creator : true,
		default : true,
		pattern : true,
		dark : true,
		access_hash : -702476988001875848,
		slug : 'hzlnkuMgiqOjCFRw',
		document : $client->documentEmpty(
			id : -3763382731686973882,
		),
		settings : $client->wallPaperSettings(
			blur : true,
			motion : true,
			background_color : 5,
			second_background_color : 40,
			third_background_color : 72,
			fourth_background_color : 51,
			intensity : 44,
			rotation : 54,
			emoticon : 'f1JByR6SruzXdcKe',
		),
	),
	stories : $client->peerStories(
		peer : $client->peerUser(
			user_id : 357884951906914442,
		),
		max_read_id : 9,
		stories : array(
			$client->storyItemDeleted(
				id : 1,
			),
			$client->storyItemSkipped(
				close_friends : true,
				id : 58,
				date : 72,
				expire_date : 68,
			),
			$client->storyItem(
				pinned : true,
				public : true,
				close_friends : true,
				min : true,
				noforwards : true,
				edited : true,
				contacts : true,
				selected_contacts : true,
				out : true,
				id : 38,
				date : 39,
				from_id : $client->peerUser(...),
				fwd_from : $client->storyFwdHeader(...),
				expire_date : 100,
				caption : 'sHmEhSden0xWFRT7',
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
				media : $client->messageMediaEmpty(...),
				media_areas : array(
					$client->mediaAreaVenue(...),
					$client->inputMediaAreaVenue(...),
					$client->mediaAreaGeoPoint(...),
					$client->mediaAreaSuggestedReaction(...),
					$client->mediaAreaChannelPost(...),
					$client->inputMediaAreaChannelPost(...),
					$client->mediaAreaUrl(...),
					$client->mediaAreaWeather(...),
					$client->mediaAreaStarGift(...),
				),
				privacy : array(
					$client->privacyValueAllowContacts(...),
					$client->privacyValueAllowAll(...),
					$client->privacyValueAllowUsers(...),
					$client->privacyValueDisallowContacts(...),
					$client->privacyValueDisallowAll(...),
					$client->privacyValueDisallowUsers(...),
					$client->privacyValueAllowChatParticipants(...),
					$client->privacyValueDisallowChatParticipants(...),
					$client->privacyValueAllowCloseFriends(...),
					$client->privacyValueAllowPremium(...),
					$client->privacyValueAllowBots(...),
					$client->privacyValueDisallowBots(...),
				),
				views : $client->storyViews(...),
				sent_reaction : $client->reactionEmpty(...),
				albums : array(76),
			),
		),
	),
	business_work_hours : $client->businessWorkHours(
		open_now : true,
		timezone_id : 'lpiumr8vKedoa4yg',
		weekly_open : array(
			$client->businessWeeklyOpen(
				start_minute : 41,
				end_minute : 6,
			),
		),
	),
	business_location : $client->businessLocation(
		geo_point : $client->geoPointEmpty(),
		address : 'eirwJzqOVDY5x8PW',
	),
	business_greeting_message : $client->businessGreetingMessage(
		shortcut_id : 57,
		recipients : $client->businessRecipients(
			existing_chats : true,
			new_chats : true,
			contacts : true,
			non_contacts : true,
			exclude_selected : true,
			users : array(6346685639274509332),
		),
		no_activity_days : 21,
	),
	business_away_message : $client->businessAwayMessage(
		offline_only : true,
		shortcut_id : 49,
		schedule : $client->businessAwayMessageScheduleAlways(),
		recipients : $client->businessRecipients(
			existing_chats : true,
			new_chats : true,
			contacts : true,
			non_contacts : true,
			exclude_selected : true,
			users : array(-335865258442631300),
		),
	),
	business_intro : $client->businessIntro(
		title : 'TltcIaYzrDkqKoCv',
		description : 'n4YbAXWTyi0BdChk',
		sticker : $client->documentEmpty(
			id : -5144734964443146674,
		),
	),
	birthday : $client->birthday(
		day : 0,
		month : 83,
		year : 16,
	),
	personal_channel_id : 380310014708811507,
	personal_channel_message : 25,
	stargifts_count : 9,
	starref_program : $client->starRefProgram(
		bot_id : -2672667780576197611,
		commission_permille : 80,
		duration_months : 93,
		end_date : 30,
		daily_revenue_per_user : $client->starsAmount(
			amount : 871696287551848348,
			nanos : 74,
		),
	),
	bot_verification : $client->botVerification(
		bot_id : -8223878322514131192,
		icon : -3763594098496235688,
		description : 'DLyYBHxVwNkd63Pv',
	),
	send_paid_messages_stars : 6019379306520579,
	disallowed_gifts : $client->disallowedGiftsSettings(
		disallow_unlimited_stargifts : true,
		disallow_limited_stargifts : true,
		disallow_unique_stargifts : true,
		disallow_premium_gifts : true,
	),
	stars_rating : $client->starsRating(
		level : 82,
		current_level_stars : 6667397827222489382,
		stars : 4818983455548414897,
		next_level_stars : -1451152057340361428,
	),
	stars_my_pending_rating : $client->starsRating(
		level : 98,
		current_level_stars : -3213325939560141099,
		stars : -8292377689049327288,
		next_level_stars : 4534617363147590390,
	),
	stars_my_pending_rating_date : 52,
);
```