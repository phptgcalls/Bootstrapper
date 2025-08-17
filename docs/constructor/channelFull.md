# channelFull

**Description** : *Full info about a channel, supergroup or gigagroup*

**Layer** : 211

```tl
channelFull#e07429de flags:# can_view_participants:flags.3?true can_set_username:flags.6?true can_set_stickers:flags.7?true hidden_prehistory:flags.10?true can_set_location:flags.16?true has_scheduled:flags.19?true can_view_stats:flags.20?true blocked:flags.22?true flags2:# can_delete_channel:flags2.0?true antispam:flags2.1?true participants_hidden:flags2.2?true translations_disabled:flags2.3?true stories_pinned_available:flags2.5?true view_forum_as_messages:flags2.6?true restricted_sponsored:flags2.11?true can_view_revenue:flags2.12?true paid_media_allowed:flags2.14?true can_view_stars_revenue:flags2.15?true paid_reactions_available:flags2.16?true stargifts_available:flags2.19?true paid_messages_available:flags2.20?true id:long about:string participants_count:flags.0?int admins_count:flags.1?int kicked_count:flags.2?int banned_count:flags.2?int online_count:flags.13?int read_inbox_max_id:int read_outbox_max_id:int unread_count:int chat_photo:Photo notify_settings:PeerNotifySettings exported_invite:flags.23?ExportedChatInvite bot_info:Vector<BotInfo> migrated_from_chat_id:flags.4?long migrated_from_max_id:flags.4?int pinned_msg_id:flags.5?int stickerset:flags.8?StickerSet available_min_id:flags.9?int folder_id:flags.11?int linked_chat_id:flags.14?long location:flags.15?ChannelLocation slowmode_seconds:flags.17?int slowmode_next_send_date:flags.18?int stats_dc:flags.12?int pts:int call:flags.21?InputGroupCall ttl_period:flags.24?int pending_suggestions:flags.25?Vector<string> groupcall_default_join_as:flags.26?Peer theme_emoticon:flags.27?string requests_pending:flags.28?int recent_requesters:flags.28?Vector<long> default_send_as:flags.29?Peer available_reactions:flags.30?ChatReactions reactions_limit:flags2.13?int stories:flags2.4?PeerStories wallpaper:flags2.7?WallPaper boosts_applied:flags2.8?int boosts_unrestrict:flags2.9?int emojiset:flags2.10?StickerSet bot_verification:flags2.17?BotVerification stargifts_count:flags2.18?int send_paid_messages_stars:flags2.21?long = ChatFull;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **can_view_participants** | [`flags.3?true`](type/true) | Can we view the participant list? |
| **can_set_username** | [`flags.6?true`](type/true) | Can we set the channel's username? |
| **can_set_stickers** | [`flags.7?true`](type/true) | Can we associate a stickerpack to the supergroup? |
| **hidden_prehistory** | [`flags.10?true`](type/true) | Is the history before we joined hidden to us? |
| **can_set_location** | [`flags.16?true`](type/true) | Can we set the geolocation of this group (for geogroups) |
| **has_scheduled** | [`flags.19?true`](type/true) | Whether scheduled messages are available |
| **can_view_stats** | [`flags.20?true`](type/true) | Can the user view channel/supergroup statistics |
| **blocked** | [`flags.22?true`](type/true) | Whether any anonymous admin of this supergroup was blocked: if set, you won't receive messages from anonymous group admins in discussion replies via @replies |
| <mark>flags2</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **can_delete_channel** | [`flags2.0?true`](type/true) | Can we delete this channel? |
| **antispam** | [`flags2.1?true`](type/true) | Whether native antispam functionality is enabled in this supergroup |
| **participants_hidden** | [`flags2.2?true`](type/true) | Whether the participant list is hidden |
| **translations_disabled** | [`flags2.3?true`](type/true) | Whether the real-time chat translation popup should be hidden |
| **stories_pinned_available** | [`flags2.5?true`](type/true) | Whether this user has some pinned stories |
| **view_forum_as_messages** | [`flags2.6?true`](type/true) | Users may also choose to display messages from all topics of a forum as if they were sent to a normal group, using a "View as messages" setting in the local client.  This setting only affects the current account, and is synced to other logged in sessions using the channels.toggleViewForumAsMessages method; invoking this method will update the value of this flag |
| **restricted_sponsored** | [`flags2.11?true`](type/true) | Whether ads on this channel were disabled as specified here » (this flag is only visible to the owner of the channel) |
| **can_view_revenue** | [`flags2.12?true`](type/true) | If set, this user can view ad revenue statistics » for this channel |
| **paid_media_allowed** | [`flags2.14?true`](type/true) | Whether the current user can send or forward paid media » to this channel |
| **can_view_stars_revenue** | [`flags2.15?true`](type/true) | If set, this user can view Telegram Star revenue statistics » for this channel |
| **paid_reactions_available** | [`flags2.16?true`](type/true) | If set, users may send paid Telegram Star reactions » to messages of this channel |
| **stargifts_available** | [`flags2.19?true`](type/true) | NOTHING |
| **paid_messages_available** | [`flags2.20?true`](type/true) | NOTHING |
| <mark>id</mark> | [`long`](type/long) | ID of the channel |
| <mark>about</mark> | [`string`](type/string) | Info about the channel |
| **participants_count** | [`flags.0?int`](type/int) | Number of participants of the channel |
| **admins_count** | [`flags.1?int`](type/int) | Number of channel admins |
| **kicked_count** | [`flags.2?int`](type/int) | Number of users kicked from the channel |
| **banned_count** | [`flags.2?int`](type/int) | Number of users banned from the channel |
| **online_count** | [`flags.13?int`](type/int) | Number of users currently online |
| <mark>read_inbox_max_id</mark> | [`int`](type/int) | Position up to which all incoming messages are read |
| <mark>read_outbox_max_id</mark> | [`int`](type/int) | Position up to which all outgoing messages are read |
| <mark>unread_count</mark> | [`int`](type/int) | Count of unread messages |
| <mark>chat_photo</mark> | [`Photo`](type/Photo) | Channel picture |
| <mark>notify_settings</mark> | [`PeerNotifySettings`](type/PeerNotifySettings) | Notification settings |
| **exported_invite** | [`flags.23?ExportedChatInvite`](type/ExportedChatInvite) | Invite link |
| <mark>bot_info</mark> | [`Vector<BotInfo>`](type/BotInfo) | Info about bots in the channel/supergroup |
| **migrated_from_chat_id** | [`flags.4?long`](type/long) | The chat ID from which this group was migrated |
| **migrated_from_max_id** | [`flags.4?int`](type/int) | The message ID in the original chat at which this group was migrated |
| **pinned_msg_id** | [`flags.5?int`](type/int) | Message ID of the last pinned message |
| **stickerset** | [`flags.8?StickerSet`](type/StickerSet) | Associated stickerset |
| **available_min_id** | [`flags.9?int`](type/int) | Identifier of a maximum unavailable message in a channel due to hidden history |
| **folder_id** | [`flags.11?int`](type/int) | Peer folder ID, for more info click here |
| **linked_chat_id** | [`flags.14?long`](type/long) | ID of the linked discussion chat for channels (and vice versa, the ID of the linked channel for discussion chats) |
| **location** | [`flags.15?ChannelLocation`](type/ChannelLocation) | Location of the geogroup |
| **slowmode_seconds** | [`flags.17?int`](type/int) | If specified, users in supergroups will only be able to send one message every slowmode_seconds seconds |
| **slowmode_next_send_date** | [`flags.18?int`](type/int) | Indicates when the user will be allowed to send another message in the supergroup (unixtime) |
| **stats_dc** | [`flags.12?int`](type/int) | If set, specifies the DC to use for fetching channel statistics |
| <mark>pts</mark> | [`int`](type/int) | Latest PTS for this channel |
| **call** | [`flags.21?InputGroupCall`](type/InputGroupCall) | Livestream or group call information |
| **ttl_period** | [`flags.24?int`](type/int) | Time-To-Live of messages in this channel or supergroup |
| **pending_suggestions** | [`flags.25?Vector<string>`](type/string) | A list of suggested actions for the supergroup admin, see here for more info » |
| **groupcall_default_join_as** | [`flags.26?Peer`](type/Peer) | When using phone.getGroupCallJoinAs to get a list of peers that can be used to join a group call, this field indicates the peer that should be selected by default |
| **theme_emoticon** | [`flags.27?string`](type/string) | Emoji representing a specific chat theme |
| **requests_pending** | [`flags.28?int`](type/int) | Pending join requests » |
| **recent_requesters** | [`flags.28?Vector<long>`](type/long) | IDs of users who requested to join recently |
| **default_send_as** | [`flags.29?Peer`](type/Peer) | Default peer used for sending messages to this channel |
| **available_reactions** | [`flags.30?ChatReactions`](type/ChatReactions) | Allowed message reactions » |
| **reactions_limit** | [`flags2.13?int`](type/int) | This flag may be used to impose a custom limit of unique reactions (i.e. a customizable version of appConfig.reactions_uniq_max) |
| **stories** | [`flags2.4?PeerStories`](type/PeerStories) | Channel stories |
| **wallpaper** | [`flags2.7?WallPaper`](type/WallPaper) | Wallpaper |
| **boosts_applied** | [`flags2.8?int`](type/int) | The number of boosts the current user has applied to the current supergroup |
| **boosts_unrestrict** | [`flags2.9?int`](type/int) | The number of boosts this supergroup requires to bypass slowmode and other restrictions, see here » for more info |
| **emojiset** | [`flags2.10?StickerSet`](type/StickerSet) | Custom emoji stickerset associated to the current supergroup, set using channels.setEmojiStickers after reaching the appropriate boost level, see here » for more info |
| **bot_verification** | [`flags2.17?BotVerification`](type/BotVerification) | NOTHING |
| **stargifts_count** | [`flags2.18?int`](type/int) | NOTHING |
| **send_paid_messages_stars** | [`flags2.21?long`](type/long) | NOTHING |

---

## Type

[ChatFull](type/ChatFull)

---

## Example

```php
$chatFull = $client->channelFull(
	can_view_participants : true,
	can_set_username : true,
	can_set_stickers : true,
	hidden_prehistory : true,
	can_set_location : true,
	has_scheduled : true,
	can_view_stats : true,
	blocked : true,
	can_delete_channel : true,
	antispam : true,
	participants_hidden : true,
	translations_disabled : true,
	stories_pinned_available : true,
	view_forum_as_messages : true,
	restricted_sponsored : true,
	can_view_revenue : true,
	paid_media_allowed : true,
	can_view_stars_revenue : true,
	paid_reactions_available : true,
	stargifts_available : true,
	paid_messages_available : true,
	id : 7247051262655242649,
	about : 'Y3WXOxTcJA61d4Dp',
	participants_count : 32,
	admins_count : 71,
	kicked_count : 82,
	banned_count : 9,
	online_count : 16,
	read_inbox_max_id : 43,
	read_outbox_max_id : 34,
	unread_count : 46,
	chat_photo : $client->photoEmpty(
		id : -3385449458560459667,
	),
	notify_settings : $client->peerNotifySettings(
		show_previews : $client->boolFalse(),
		silent : $client->boolFalse(),
		mute_until : 11,
		ios_sound : $client->notificationSoundDefault(),
		android_sound : $client->notificationSoundDefault(),
		other_sound : $client->notificationSoundDefault(),
		stories_muted : $client->boolFalse(),
		stories_hide_sender : $client->boolFalse(),
		stories_ios_sound : $client->notificationSoundDefault(),
		stories_android_sound : $client->notificationSoundDefault(),
		stories_other_sound : $client->notificationSoundDefault(),
	),
	exported_invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'SIDp6bUvsxg2mK9h',
		admin_id : -1478967231227164271,
		date : 43,
		start_date : 35,
		expire_date : 74,
		usage_limit : 83,
		usage : 22,
		requested : 8,
		subscription_expired : 19,
		title : 'cUOTGKuIgRmkxlX6',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 13,
			amount : -3183492478915293165,
		),
	),
	bot_info : array(
		$client->botInfo(
			has_preview_medias : true,
			user_id : 6711099782310165648,
			description : 'AX7kG6H2jxUCIc1u',
			description_photo : $client->photoEmpty(
				id : 7415431738421128131,
			),
			description_document : $client->documentEmpty(
				id : 6275068496135257386,
			),
			commands : array(
				$client->botCommand(
					command : 'nWVI4C1aEdrRuw2X',
					description : 'W75xnwgMjoH0Ub4p',
				),
			),
			menu_button : $client->botMenuButtonDefault(),
			privacy_policy_url : 'https://docs.liveproto.dev',
			app_settings : $client->botAppSettings(
				placeholder_path : '?iO)6LiveProto?HQ8[',
				background_color : 13,
				background_dark_color : 13,
				header_color : 22,
				header_dark_color : 61,
			),
			verifier_settings : $client->botVerifierSettings(
				can_modify_custom_description : true,
				icon : -3725267929958099521,
				company : 'WfJiyzIak89ej2qC',
				custom_description : 'H2hZokYa638L1Sc9',
			),
		),
	),
	migrated_from_chat_id : 7054466080481430795,
	migrated_from_max_id : 94,
	pinned_msg_id : 53,
	stickerset : $client->stickerSet(
		archived : true,
		official : true,
		masks : true,
		emojis : true,
		text_color : true,
		channel_emoji_status : true,
		creator : true,
		installed_date : 53,
		id : -5144297006457528286,
		access_hash : 5842172030070632636,
		title : 'egPTaq0349nhtQDC',
		short_name : '58mirp9yVbA73RDT',
		thumbs : array(
			$client->photoSizeEmpty(
				type : '7bWRXIDyo3uJAQ8Z',
			),
			$client->photoSize(
				type : 'mDpauN0EkyzwSY8O',
				w : 73,
				h : 2,
				size : 88,
			),
			$client->photoCachedSize(
				type : 'YdiabSVe9IvCx1AZ',
				w : 21,
				h : 50,
				bytes : '$*?LiveProto??QO?',
			),
			$client->photoStrippedSize(
				type : 'HtkwfysThvocmgXl',
				bytes : '֓r??LiveProtoP?&?',
			),
			$client->photoSizeProgressive(
				type : 'i8DflM3UtXsI4TSw',
				w : 76,
				h : 0,
				sizes : array(21),
			),
			$client->photoPathSize(
				type : 'yw3f0zjxrhgCO26U',
				bytes : 'XBD?LiveProto$j?D',
			),
		),
		thumb_dc_id : 36,
		thumb_version : 9,
		thumb_document_id : 8796090676119628399,
		count : 82,
		hash : 1,
	),
	available_min_id : 59,
	folder_id : 3,
	linked_chat_id : 5073416232513124597,
	location : $client->channelLocationEmpty(),
	slowmode_seconds : 80,
	slowmode_next_send_date : 21,
	stats_dc : 51,
	pts : 54,
	call : $client->inputGroupCall(
		id : 2830305978391386989,
		access_hash : 5195799879056774519,
	),
	ttl_period : 78,
	pending_suggestions : array('H9cEy4VhapegrRAP'),
	groupcall_default_join_as : $client->peerUser(
		user_id : -1135127040681882778,
	),
	theme_emoticon : 'HfPwsLgNSOETXIz6',
	requests_pending : 61,
	recent_requesters : array(-6044802374884904332),
	default_send_as : $client->peerUser(
		user_id : 4293326442359464394,
	),
	available_reactions : $client->chatReactionsNone(),
	reactions_limit : 22,
	stories : $client->peerStories(
		peer : $client->peerUser(
			user_id : 6562595019313895149,
		),
		max_read_id : 41,
		stories : array(
			$client->storyItemDeleted(
				id : 83,
			),
			$client->storyItemSkipped(
				close_friends : true,
				id : 69,
				date : 94,
				expire_date : 19,
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
				id : 78,
				date : 77,
				from_id : $client->peerUser(...),
				fwd_from : $client->storyFwdHeader(...),
				expire_date : 30,
				caption : 'z8EFtYBRVKcDWylx',
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
				albums : array(34),
			),
		),
	),
	wallpaper : $client->wallPaper(
		id : 7268057938155808891,
		creator : true,
		default : true,
		pattern : true,
		dark : true,
		access_hash : 7894271507071116990,
		slug : 'ALfIOgW4tR0UX6M7',
		document : $client->documentEmpty(
			id : 2354294445107517120,
		),
		settings : $client->wallPaperSettings(
			blur : true,
			motion : true,
			background_color : 11,
			second_background_color : 91,
			third_background_color : 54,
			fourth_background_color : 65,
			intensity : 8,
			rotation : 14,
			emoticon : 'S7X0JmbfxpWP5eEu',
		),
	),
	boosts_applied : 30,
	boosts_unrestrict : 27,
	emojiset : $client->stickerSet(
		archived : true,
		official : true,
		masks : true,
		emojis : true,
		text_color : true,
		channel_emoji_status : true,
		creator : true,
		installed_date : 91,
		id : 6282619069587314379,
		access_hash : 5143129117938925224,
		title : 'bJ85fIzqlW4c9PYH',
		short_name : 'LebC82hRIETw0f4J',
		thumbs : array(
			$client->photoSizeEmpty(
				type : 'Aa0Ijr5gNscUBo98',
			),
			$client->photoSize(
				type : 'bDsOhR5yjoLCeWvt',
				w : 79,
				h : 58,
				size : 49,
			),
			$client->photoCachedSize(
				type : 'LtROQ4YDv0ipCUrF',
				w : 71,
				h : 32,
				bytes : 'CO	?LiveProtoE' . "\0" . '??',
			),
			$client->photoStrippedSize(
				type : '17rsujp8kiXCH3yN',
				bytes : 'g??1?LiveProto"?Q?',
			),
			$client->photoSizeProgressive(
				type : '9x5IUElinYy6uAWD',
				w : 67,
				h : 52,
				sizes : array(73),
			),
			$client->photoPathSize(
				type : '1KpwfBWCtOQzSxch',
				bytes : '7??4LiveProto???',
			),
		),
		thumb_dc_id : 42,
		thumb_version : 90,
		thumb_document_id : -4982067714561151918,
		count : 90,
		hash : 62,
	),
	bot_verification : $client->botVerification(
		bot_id : -8922188782609866853,
		icon : -4657665367055072064,
		description : 'XrAhPvEt6Q7Ulcpn',
	),
	stargifts_count : 82,
	send_paid_messages_stars : 2408750165607765242,
);
```