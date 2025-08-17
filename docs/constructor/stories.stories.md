# stories.stories

**Description** : *List of stories*

**Layer** : 211

```tl
stories.stories#63c3dd0a flags:# count:int stories:Vector<StoryItem> pinned_to_top:flags.0?Vector<int> chats:Vector<Chat> users:Vector<User> = stories.Stories;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of stories that can be fetched |
| <mark>stories</mark> | [`Vector<StoryItem>`](type/StoryItem) | Stories |
| **pinned_to_top** | [`flags.0?Vector<int>`](type/int) | IDs of pinned stories |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[stories.Stories](type/stories.Stories)

---

## Example

```php
$storiesStories = $client->stories->stories(
	count : 4,
	stories : array(
		$client->storyItemDeleted(
			id : 26,
		),
		$client->storyItemSkipped(
			close_friends : true,
			id : 88,
			date : 8,
			expire_date : 2,
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
			id : 4,
			date : 52,
			from_id : $client->peerUser(
				user_id : -6664775652782905261,
			),
			fwd_from : $client->storyFwdHeader(
				modified : true,
				from : $client->peerUser(...),
				from_name : '8cqk2HTENRMYSU1C',
				story_id : 38,
			),
			expire_date : 45,
			caption : 'qufrWF13Isp7SCgG',
			entities : array(
				$client->messageEntityUnknown(
					offset : 80,
					length : 10,
				),
				$client->messageEntityMention(
					offset : 81,
					length : 13,
				),
				$client->messageEntityHashtag(
					offset : 19,
					length : 19,
				),
				$client->messageEntityBotCommand(
					offset : 1,
					length : 7,
				),
				$client->messageEntityUrl(
					offset : 35,
					length : 91,
				),
				$client->messageEntityEmail(
					offset : 91,
					length : 86,
				),
				$client->messageEntityBold(
					offset : 13,
					length : 7,
				),
				$client->messageEntityItalic(
					offset : 71,
					length : 77,
				),
				$client->messageEntityCode(
					offset : 38,
					length : 41,
				),
				$client->messageEntityPre(
					offset : 33,
					length : 28,
					language : '2CjzlTOb5H7fDJEc',
				),
				$client->messageEntityTextUrl(
					offset : 25,
					length : 23,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 51,
					length : 87,
					user_id : -2968717948977804174,
				),
				$client->inputMessageEntityMentionName(
					offset : 59,
					length : 25,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 21,
					length : 18,
				),
				$client->messageEntityCashtag(
					offset : 77,
					length : 69,
				),
				$client->messageEntityUnderline(
					offset : 4,
					length : 82,
				),
				$client->messageEntityStrike(
					offset : 21,
					length : 69,
				),
				$client->messageEntityBankCard(
					offset : 35,
					length : 43,
				),
				$client->messageEntitySpoiler(
					offset : 92,
					length : 15,
				),
				$client->messageEntityCustomEmoji(
					offset : 49,
					length : 73,
					document_id : -8513796166809043683,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 1,
					length : 51,
				),
			),
			media : $client->messageMediaEmpty(),
			media_areas : array(
				$client->mediaAreaVenue(
					coordinates : $client->mediaAreaCoordinates(...),
					geo : $client->geoPointEmpty(...),
					title : 'dKsbth0xSOron4A9',
					address : 'GXadQkwvjELftOD1',
					provider : '8BgH073Li9yUQTtM',
					venue_id : 'HhaLnZVyDSFwlUum',
					venue_type : 'XqR20dYMm8hHUAKb',
				),
				$client->inputMediaAreaVenue(
					coordinates : $client->mediaAreaCoordinates(...),
					query_id : 8403332679606403125,
					result_id : 'Djgch3q5kZrwpxda',
				),
				$client->mediaAreaGeoPoint(
					coordinates : $client->mediaAreaCoordinates(...),
					geo : $client->geoPointEmpty(...),
					address : $client->geoPointAddress(...),
				),
				$client->mediaAreaSuggestedReaction(
					dark : true,
					flipped : true,
					coordinates : $client->mediaAreaCoordinates(...),
					reaction : $client->reactionEmpty(...),
				),
				$client->mediaAreaChannelPost(
					coordinates : $client->mediaAreaCoordinates(...),
					channel_id : -2305799412034197625,
					msg_id : 8,
				),
				$client->inputMediaAreaChannelPost(
					coordinates : $client->mediaAreaCoordinates(...),
					channel : $client->inputChannelEmpty(...),
					msg_id : 86,
				),
				$client->mediaAreaUrl(
					coordinates : $client->mediaAreaCoordinates(...),
					url : 'https://docs.liveproto.dev',
				),
				$client->mediaAreaWeather(
					coordinates : $client->mediaAreaCoordinates(...),
					emoji : 'H42DTi7ce9qx1VoF',
					temperature_c : -1832023.3388671875,
					color : 92,
				),
				$client->mediaAreaStarGift(
					coordinates : $client->mediaAreaCoordinates(...),
					slug : 'cfiFQ8jMHbYVs6mv',
				),
			),
			privacy : array(
				$client->privacyValueAllowContacts(),
				$client->privacyValueAllowAll(),
				$client->privacyValueAllowUsers(
					users : array(2116443394968710235),
				),
				$client->privacyValueDisallowContacts(),
				$client->privacyValueDisallowAll(),
				$client->privacyValueDisallowUsers(
					users : array(4023281652997439701),
				),
				$client->privacyValueAllowChatParticipants(
					chats : array(3761190096670429308),
				),
				$client->privacyValueDisallowChatParticipants(
					chats : array(-706317554016036810),
				),
				$client->privacyValueAllowCloseFriends(),
				$client->privacyValueAllowPremium(),
				$client->privacyValueAllowBots(),
				$client->privacyValueDisallowBots(),
			),
			views : $client->storyViews(
				has_viewers : true,
				views_count : 72,
				forwards_count : 18,
				reactions : array(
					$client->reactionCount(...),
				),
				reactions_count : 98,
				recent_viewers : array(4057035454061110805),
			),
			sent_reaction : $client->reactionEmpty(),
			albums : array(52),
		),
	),
	pinned_to_top : array(96),
	chats : array(
		$client->chatEmpty(
			id : 8522190900953192615,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -2326352605676487532,
			title : 'H1jzr6yopaBJl5bG',
			photo : $client->chatPhotoEmpty(),
			participants_count : 28,
			date : 72,
			version : 6,
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
				until_date : 97,
			),
		),
		$client->chatForbidden(
			id : -2596099660808837260,
			title : '37FNck5C0L9AyBwQ',
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
			id : -5769655865118176216,
			access_hash : 5741439772084597622,
			title : 'UfleCOKnraxqvDuy',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 57,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Vbx8uEqydvZC5GUA',
					reason : 'WcxJrRsTDejBXnb0',
					text : 'TQzlFrP2itBe5NJc',
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
				until_date : 83,
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
				until_date : 60,
			),
			participants_count : 52,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 52,
			color : $client->peerColor(
				color : 97,
				background_emoji_id : 1933219448121963780,
			),
			profile_color : $client->peerColor(
				color : 9,
				background_emoji_id : 4432602970456024113,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 28,
			subscription_until_date : 30,
			bot_verification_icon : -6980608607900937399,
			send_paid_messages_stars : -7101090838391500647,
			linked_monoforum_id : -916336802154961241,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -3134026748183311289,
			access_hash : 4788140367310662868,
			title : 'X27zy5jmc6IAu8O3',
			until_date : 90,
		),
	),
	users : array(
		$client->userEmpty(
			id : -2949087288565685987,
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
			id : 2790720667120046070,
			access_hash : 3361948362920236840,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 53,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'G40tgDNImHb8vzow',
					reason : 'oW9mpHkQLOR5rswK',
					text : '9Z5if6LntC1Twk8I',
				),
			),
			bot_inline_placeholder : '2HmulpsKoWRPOrL1',
			lang_code : 'LNCaxh8Kwsdpf574',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 93,
			color : $client->peerColor(
				color : 5,
				background_emoji_id : -2121445224602381965,
			),
			profile_color : $client->peerColor(
				color : 81,
				background_emoji_id : 7392572561023638582,
			),
			bot_active_users : 19,
			bot_verification_icon : 6348237334731309826,
			send_paid_messages_stars : 1138872047006005520,
		),
	),
);
```