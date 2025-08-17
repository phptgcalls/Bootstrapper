# updatesCombined

**Description** : *Constructor for a group of updates*

**Layer** : 211

```tl
updatesCombined#725b04c3 updates:Vector<Update> users:Vector<User> chats:Vector<Chat> date:int seq_start:int seq:int = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>updates</mark> | [`Vector<Update>`](type/Update) | List of updates |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of users mentioned in updates |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | List of chats mentioned in updates |
| <mark>date</mark> | [`int`](type/int) | Current date |
| <mark>seq_start</mark> | [`int`](type/int) | Value seq for the earliest update in a group |
| <mark>seq</mark> | [`int`](type/int) | Value seq for the latest update in a group |

---

## Type

[Updates](type/Updates)

---

## Example

```php
$updates = $client->updatesCombined(
	updates : array(
		$client->updateNewMessage(
			message : $client->messageEmpty(
				id : 36,
				peer_id : $client->peerUser(...),
			),
			pts : 10,
			pts_count : 64,
		),
		$client->updateMessageID(
			id : 58,
			random_id : 8437135574419706578,
		),
		$client->updateDeleteMessages(
			messages : array(6),
			pts : 63,
			pts_count : 51,
		),
		$client->updateUserTyping(
			user_id : 6034415884543753247,
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatUserTyping(
			chat_id : 1409458563465830012,
			from_id : $client->peerUser(
				user_id : 3050944087419474015,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatParticipants(
			participants : $client->chatParticipantsForbidden(
				chat_id : -7324489179268677421,
				self_participant : $client->chatParticipant(...),
			),
		),
		$client->updateUserStatus(
			user_id : 9041564511438563929,
			status : $client->userStatusEmpty(),
		),
		$client->updateUserName(
			user_id : 2625139236938908324,
			first_name : 'Tak',
			last_name : 'None',
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
		),
		$client->updateNewAuthorization(
			unconfirmed : true,
			hash : 6159198671058859890,
			date : 28,
			device : 'tnTE2wZ6KisdgljL',
			location : 'aEbfACJ2PhUHSxyc',
		),
		$client->updateNewEncryptedMessage(
			message : $client->encryptedMessage(
				random_id : -1436480253959546497,
				chat_id : 21,
				date : 99,
				bytes : '???LiveProto?B???',
				file : $client->encryptedFileEmpty(...),
			),
			qts : 24,
		),
		$client->updateEncryptedChatTyping(
			chat_id : 29,
		),
		$client->updateEncryption(
			chat : $client->encryptedChatEmpty(
				id : 26,
			),
			date : 58,
		),
		$client->updateEncryptedMessagesRead(
			chat_id : 62,
			max_date : 61,
			date : 47,
		),
		$client->updateChatParticipantAdd(
			chat_id : -5507910936974505253,
			user_id : -3930387441714967457,
			inviter_id : -2422753562536352709,
			date : 85,
			version : 8,
		),
		$client->updateChatParticipantDelete(
			chat_id : -8285958352480145891,
			user_id : 2067378132497690047,
			version : 9,
		),
		$client->updateDcOptions(
			dc_options : array(
				$client->dcOption(
					ipv6 : true,
					media_only : true,
					tcpo_only : true,
					cdn : true,
					static : true,
					this_port_only : true,
					id : 2,
					ip_address : '127.0.0.1',
					port : 83,
					secret : 'n_??2LiveProto?V֋&',
				),
			),
		),
		$client->updateNotifySettings(
			peer : $client->notifyPeer(
				peer : $client->peerUser(...),
			),
			notify_settings : $client->peerNotifySettings(
				show_previews : $client->boolFalse(...),
				silent : $client->boolFalse(...),
				mute_until : 10,
				ios_sound : $client->notificationSoundDefault(...),
				android_sound : $client->notificationSoundDefault(...),
				other_sound : $client->notificationSoundDefault(...),
				stories_muted : $client->boolFalse(...),
				stories_hide_sender : $client->boolFalse(...),
				stories_ios_sound : $client->notificationSoundDefault(...),
				stories_android_sound : $client->notificationSoundDefault(...),
				stories_other_sound : $client->notificationSoundDefault(...),
			),
		),
		$client->updateServiceNotification(
			popup : true,
			invert_media : true,
			inbox_date : 36,
			type : 'LDod2ZyRNks3Mi4t',
			message : 'xYTuXPBjlz6QiMcJ',
			media : $client->messageMediaEmpty(),
			entities : array(
				$client->messageEntityUnknown(
					offset : 56,
					length : 92,
				),
				$client->messageEntityMention(
					offset : 74,
					length : 82,
				),
				$client->messageEntityHashtag(
					offset : 77,
					length : 81,
				),
				$client->messageEntityBotCommand(
					offset : 63,
					length : 13,
				),
				$client->messageEntityUrl(
					offset : 46,
					length : 72,
				),
				$client->messageEntityEmail(
					offset : 15,
					length : 74,
				),
				$client->messageEntityBold(
					offset : 47,
					length : 19,
				),
				$client->messageEntityItalic(
					offset : 6,
					length : 34,
				),
				$client->messageEntityCode(
					offset : 10,
					length : 2,
				),
				$client->messageEntityPre(
					offset : 94,
					length : 18,
					language : '6sO9qYNt3x1FMEVL',
				),
				$client->messageEntityTextUrl(
					offset : 72,
					length : 95,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 90,
					length : 4,
					user_id : 4824935158144510378,
				),
				$client->inputMessageEntityMentionName(
					offset : 91,
					length : 92,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 99,
					length : 59,
				),
				$client->messageEntityCashtag(
					offset : 97,
					length : 79,
				),
				$client->messageEntityUnderline(
					offset : 21,
					length : 83,
				),
				$client->messageEntityStrike(
					offset : 91,
					length : 94,
				),
				$client->messageEntityBankCard(
					offset : 60,
					length : 21,
				),
				$client->messageEntitySpoiler(
					offset : 90,
					length : 58,
				),
				$client->messageEntityCustomEmoji(
					offset : 6,
					length : 32,
					document_id : -944942328986145050,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 68,
					length : 6,
				),
			),
		),
		$client->updatePrivacy(
			key : $client->privacyKeyStatusTimestamp(),
			rules : array(
				$client->privacyValueAllowContacts(),
				$client->privacyValueAllowAll(),
				$client->privacyValueAllowUsers(
					users : array(8570141535670157345),
				),
				$client->privacyValueDisallowContacts(),
				$client->privacyValueDisallowAll(),
				$client->privacyValueDisallowUsers(
					users : array(3388645916589441499),
				),
				$client->privacyValueAllowChatParticipants(
					chats : array(-4575403786431386572),
				),
				$client->privacyValueDisallowChatParticipants(
					chats : array(-7788436399414992789),
				),
				$client->privacyValueAllowCloseFriends(),
				$client->privacyValueAllowPremium(),
				$client->privacyValueAllowBots(),
				$client->privacyValueDisallowBots(),
			),
		),
		$client->updateUserPhone(
			user_id : 1642829623194934711,
			phone : '+1234567890',
		),
		$client->updateReadHistoryInbox(
			folder_id : 83,
			peer : $client->peerUser(
				user_id : -4323747469572876957,
			),
			max_id : 55,
			still_unread_count : 86,
			pts : 0,
			pts_count : 4,
		),
		$client->updateReadHistoryOutbox(
			peer : $client->peerUser(
				user_id : 8258317528122556365,
			),
			max_id : 76,
			pts : 98,
			pts_count : 40,
		),
		$client->updateWebPage(
			webpage : $client->webPageEmpty(
				id : -4091903981792350847,
				url : 'https://docs.liveproto.dev',
			),
			pts : 86,
			pts_count : 6,
		),
		$client->updateReadMessagesContents(
			messages : array(29),
			pts : 80,
			pts_count : 8,
			date : 0,
		),
		$client->updateChannelTooLong(
			channel_id : 5207148993175426576,
			pts : 38,
		),
		$client->updateChannel(
			channel_id : 608818679536252015,
		),
		$client->updateNewChannelMessage(
			message : $client->messageEmpty(
				id : 78,
				peer_id : $client->peerUser(...),
			),
			pts : 83,
			pts_count : 75,
		),
		$client->updateReadChannelInbox(
			folder_id : 6,
			channel_id : 5585633669544973024,
			max_id : 70,
			still_unread_count : 43,
			pts : 84,
		),
		$client->updateDeleteChannelMessages(
			channel_id : -3436481616352138968,
			messages : array(19),
			pts : 56,
			pts_count : 54,
		),
		$client->updateChannelMessageViews(
			channel_id : 2452909302909566987,
			id : 81,
			views : 29,
		),
		$client->updateChatParticipantAdmin(
			chat_id : 4715115021539916392,
			user_id : -4425579978589324320,
			is_admin : $client->boolFalse(),
			version : 23,
		),
		$client->updateNewStickerSet(
			stickerset : $client->messages->stickerSet(
				set : $client->stickerSet(...),
				packs : array(
					$client->stickerPack(...),
				),
				keywords : array(
					$client->stickerKeyword(...),
				),
				documents : array(
					$client->documentEmpty(...),
					$client->document(...),
				),
			),
		),
		$client->updateStickerSetsOrder(
			masks : true,
			emojis : true,
			order : array(-2072264054403119710),
		),
		$client->updateStickerSets(
			masks : true,
			emojis : true,
		),
		$client->updateSavedGifs(),
		$client->updateBotInlineQuery(
			query_id : -5521542345656983493,
			user_id : -8619348454110082546,
			query : 'AItvo6r4UR0wQ1Os',
			geo : $client->geoPointEmpty(),
			peer_type : $client->inlineQueryPeerTypeSameBotPM(),
			offset : 'YmLZQV0c4z91pMad',
		),
		$client->updateBotInlineSend(
			user_id : 5526564342878025624,
			query : 'lGwUC28Wtf5Oe1dm',
			geo : $client->geoPointEmpty(),
			id : 'd4zL70ykR5m2vcIK',
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 4,
				id : -1476790206983910764,
				access_hash : -7916332207929484570,
			),
		),
		$client->updateEditChannelMessage(
			message : $client->messageEmpty(
				id : 91,
				peer_id : $client->peerUser(...),
			),
			pts : 72,
			pts_count : 76,
		),
		$client->updateBotCallbackQuery(
			query_id : -6328221230423452585,
			user_id : -8839823569738581548,
			peer : $client->peerUser(
				user_id : -6356489746863676506,
			),
			msg_id : 78,
			chat_instance : -5957130971550860166,
			data : 'D?؄LiveProto?????',
			game_short_name : 'lDmNIKdfqAs2c3vT',
		),
		$client->updateEditMessage(
			message : $client->messageEmpty(
				id : 51,
				peer_id : $client->peerUser(...),
			),
			pts : 48,
			pts_count : 37,
		),
		$client->updateInlineBotCallbackQuery(
			query_id : 5870733995756550473,
			user_id : 1648631363923200998,
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 96,
				id : -2020910566658365647,
				access_hash : -7551241343937694097,
			),
			chat_instance : 4421655973878406502,
			data : 'My?k"LiveProto??*?0',
			game_short_name : 'MBZeslJ6ENudp0ox',
		),
		$client->updateReadChannelOutbox(
			channel_id : -2917513934049819110,
			max_id : 57,
		),
		$client->updateDraftMessage(
			peer : $client->peerUser(
				user_id : 90083643578888085,
			),
			top_msg_id : 8,
			saved_peer_id : $client->peerUser(
				user_id : -3936485132717317138,
			),
			draft : $client->draftMessageEmpty(
				date : 49,
			),
		),
		$client->updateReadFeaturedStickers(),
		$client->updateRecentStickers(),
		$client->updateConfig(),
		$client->updatePtsChanged(),
		$client->updateChannelWebPage(
			channel_id : 3168418619377258032,
			webpage : $client->webPageEmpty(
				id : 8776519454717452198,
				url : 'https://docs.liveproto.dev',
			),
			pts : 19,
			pts_count : 31,
		),
		$client->updateDialogPinned(
			pinned : true,
			folder_id : 43,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
		),
		$client->updatePinnedDialogs(
			folder_id : 73,
			order : array(
				$client->dialogPeer(
					peer : $client->peerUser(...),
				),
				$client->dialogPeerFolder(
					folder_id : 28,
				),
			),
		),
		$client->updateBotWebhookJSON(
			data : $client->dataJSON(
				data : '32tRW1h7pvKG6ETV',
			),
		),
		$client->updateBotWebhookJSONQuery(
			query_id : -4712559187566320808,
			data : $client->dataJSON(
				data : '7TZthPxMq3fvEnUV',
			),
			timeout : 35,
		),
		$client->updateBotShippingQuery(
			query_id : -4280644475958837666,
			user_id : -2534605248711688918,
			payload : '??ƩnLiveProtogn?x',
			shipping_address : $client->postAddress(
				street_line1 : 'Z8YU9MqgrnRz0E4N',
				street_line2 : 'QZna0LPKei76BEYo',
				city : 'CZFwNKhjidcIHBxY',
				state : 'yj1mLw9g0l8kIdqH',
				country_iso2 : 'EhlRQYtDxOL8o6He',
				post_code : 'lRU3xBogEJDbniSQ',
			),
		),
		$client->updateBotPrecheckoutQuery(
			query_id : 1418655729475187645,
			user_id : -4492089885067029994,
			payload : '?u???LiveProto????c',
			info : $client->paymentRequestedInfo(
				name : 'ZjGs1CqzpAkhMaNB',
				phone : '+1234567890',
				email : 'reply@liveproto.dev',
				shipping_address : $client->postAddress(...),
			),
			shipping_option_id : 'fg4HOuVYcP3QbReW',
			currency : 'x1NBwbD3UhS7A94C',
			total_amount : 6742208445957097432,
		),
		$client->updatePhoneCall(
			phone_call : $client->phoneCallEmpty(
				id : 8843058736943202222,
			),
		),
		$client->updateLangPackTooLong(
			lang_code : '3m6bapZCIRwUY5nW',
		),
		$client->updateLangPack(
			difference : $client->langPackDifference(
				lang_code : 'QR3jdiuFGWHO1EIz',
				from_version : 35,
				version : 23,
				strings : array(
					$client->langPackString(...),
					$client->langPackStringPluralized(...),
					$client->langPackStringDeleted(...),
				),
			),
		),
		$client->updateFavedStickers(),
		$client->updateChannelReadMessagesContents(
			channel_id : -76437816079370280,
			top_msg_id : 39,
			saved_peer_id : $client->peerUser(
				user_id : -6096829258952004895,
			),
			messages : array(71),
		),
		$client->updateContactsReset(),
		$client->updateChannelAvailableMessages(
			channel_id : 6848865957265876683,
			available_min_id : 29,
		),
		$client->updateDialogUnreadMark(
			unread : true,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
			saved_peer_id : $client->peerUser(
				user_id : 94931470530019135,
			),
		),
		$client->updateMessagePoll(
			poll_id : 4318001557267705912,
			poll : $client->poll(
				id : 2244973133139286506,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 53,
				close_date : 15,
			),
			results : $client->pollResults(
				min : true,
				results : array(
					$client->pollAnswerVoters(...),
				),
				total_voters : 75,
				recent_voters : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				solution : 'Pt2pksxBOdYVRhL1',
				solution_entities : array(
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
		$client->updateChatDefaultBannedRights(
			peer : $client->peerUser(
				user_id : -5271789267880257639,
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
				until_date : 32,
			),
			version : 71,
		),
		$client->updateFolderPeers(
			folder_peers : array(
				$client->folderPeer(
					peer : $client->peerUser(...),
					folder_id : 36,
				),
			),
			pts : 9,
			pts_count : 37,
		),
		$client->updatePeerSettings(
			peer : $client->peerUser(
				user_id : 5312629300572202766,
			),
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
				geo_distance : 34,
				request_chat_title : 'YPslI45zW3FTN1Hc',
				request_chat_date : 5,
				business_bot_id : 7736970530826891362,
				business_bot_manage_url : 'https://docs.liveproto.dev',
				charge_paid_message_stars : 7385001134044803792,
				registration_month : 'rE98dVjmKZLTRqQi',
				phone_country : '+1234567890',
				name_change_date : 64,
				photo_change_date : 38,
			),
		),
		$client->updatePeerLocated(
			peers : array(
				$client->peerLocated(
					peer : $client->peerUser(...),
					expires : 24,
					distance : 27,
				),
				$client->peerSelfLocated(
					expires : 68,
				),
			),
		),
		$client->updateNewScheduledMessage(
			message : $client->messageEmpty(
				id : 8,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteScheduledMessages(
			peer : $client->peerUser(
				user_id : -4109321993879007730,
			),
			messages : array(18),
			sent_messages : array(8),
		),
		$client->updateTheme(
			theme : $client->theme(
				creator : true,
				default : true,
				for_chat : true,
				id : 5111625243712943041,
				access_hash : -7719022163411404059,
				slug : 'qbBtUMlwHPTgF62J',
				title : '3Gmo1J4QfCyADELk',
				document : $client->documentEmpty(...),
				settings : array(
					$client->themeSettings(...),
				),
				emoticon : 'nIi0RLWcZaE2pvhs',
				installs_count : 7,
			),
		),
		$client->updateGeoLiveViewed(
			peer : $client->peerUser(
				user_id : -6890667309653778248,
			),
			msg_id : 22,
		),
		$client->updateLoginToken(),
		$client->updateMessagePollVote(
			poll_id : 380856083973151202,
			peer : $client->peerUser(
				user_id : 1228695351552316814,
			),
			options : array('?e???LiveProtor????'),
			qts : 58,
		),
		$client->updateDialogFilter(
			id : 81,
			filter : $client->dialogFilter(
				contacts : true,
				non_contacts : true,
				groups : true,
				broadcasts : true,
				bots : true,
				exclude_muted : true,
				exclude_read : true,
				exclude_archived : true,
				title_noanimate : true,
				id : 61,
				title : $client->textWithEntities(...),
				emoticon : 'OHgA7F0uKkqS2h8s',
				color : 42,
				pinned_peers : array(
					$client->inputPeerEmpty(...),
					$client->inputPeerSelf(...),
					$client->inputPeerChat(...),
					$client->inputPeerUser(...),
					$client->inputPeerChannel(...),
					$client->inputPeerUserFromMessage(...),
					$client->inputPeerChannelFromMessage(...),
				),
				include_peers : array(
					$client->inputPeerEmpty(...),
					$client->inputPeerSelf(...),
					$client->inputPeerChat(...),
					$client->inputPeerUser(...),
					$client->inputPeerChannel(...),
					$client->inputPeerUserFromMessage(...),
					$client->inputPeerChannelFromMessage(...),
				),
				exclude_peers : array(
					$client->inputPeerEmpty(...),
					$client->inputPeerSelf(...),
					$client->inputPeerChat(...),
					$client->inputPeerUser(...),
					$client->inputPeerChannel(...),
					$client->inputPeerUserFromMessage(...),
					$client->inputPeerChannelFromMessage(...),
				),
			),
		),
		$client->updateDialogFilterOrder(
			order : array(85),
		),
		$client->updateDialogFilters(),
		$client->updatePhoneCallSignalingData(
			phone_call_id : -5227531469587966231,
			data : '\'??BLiveProto?w?H',
		),
		$client->updateChannelMessageForwards(
			channel_id : 2806971453339077835,
			id : 71,
			forwards : 34,
		),
		$client->updateReadChannelDiscussionInbox(
			channel_id : 3068528738663204408,
			top_msg_id : 9,
			read_max_id : 51,
			broadcast_id : -1274263697575293369,
			broadcast_post : 71,
		),
		$client->updateReadChannelDiscussionOutbox(
			channel_id : 4088933832728232961,
			top_msg_id : 70,
			read_max_id : 6,
		),
		$client->updatePeerBlocked(
			blocked : true,
			blocked_my_stories_from : true,
			peer_id : $client->peerUser(
				user_id : 663350054693942931,
			),
		),
		$client->updateChannelUserTyping(
			channel_id : -7293740575624135240,
			top_msg_id : 16,
			from_id : $client->peerUser(
				user_id : 8191417514811003181,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updatePinnedMessages(
			pinned : true,
			peer : $client->peerUser(
				user_id : -6388086843403622022,
			),
			messages : array(39),
			pts : 43,
			pts_count : 23,
		),
		$client->updatePinnedChannelMessages(
			pinned : true,
			channel_id : 2507624905265056223,
			messages : array(13),
			pts : 29,
			pts_count : 81,
		),
		$client->updateChat(
			chat_id : 4314261399127345212,
		),
		$client->updateGroupCallParticipants(
			call : $client->inputGroupCall(
				id : -4728395164967719423,
				access_hash : 3410993126317156226,
			),
			participants : array(
				$client->groupCallParticipant(
					muted : true,
					left : true,
					can_self_unmute : true,
					just_joined : true,
					versioned : true,
					min : true,
					muted_by_you : true,
					volume_by_admin : true,
					self : true,
					video_joined : true,
					peer : $client->peerUser(...),
					date : 97,
					active_date : 45,
					source : 33,
					volume : 70,
					about : 'XdvinmxPYhpDWl4s',
					raise_hand_rating : -2510017353564286598,
					video : $client->groupCallParticipantVideo(...),
					presentation : $client->groupCallParticipantVideo(...),
				),
			),
			version : 27,
		),
		$client->updateGroupCall(
			chat_id : 116818144102829449,
			call : $client->groupCallDiscarded(
				id : -5845817416233765547,
				access_hash : -338636742484690156,
				duration : 57,
			),
		),
		$client->updatePeerHistoryTTL(
			peer : $client->peerUser(
				user_id : -7953716098763428976,
			),
			ttl_period : 27,
		),
		$client->updateChatParticipant(
			chat_id : 4753170581492036766,
			date : 55,
			actor_id : -6099047129581615865,
			user_id : -4101670619599241114,
			prev_participant : $client->chatParticipant(
				user_id : 4295394061152523748,
				inviter_id : -2298961537660059474,
				date : 8,
			),
			new_participant : $client->chatParticipant(
				user_id : -3254492251492900192,
				inviter_id : 4839443535349277965,
				date : 64,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'OMfgGXHPhkcJs6Ex',
				admin_id : -4732569633579806225,
				date : 55,
				start_date : 83,
				expire_date : 36,
				usage_limit : 28,
				usage : 55,
				requested : 79,
				subscription_expired : 95,
				title : 'i6a20DcMUCErNupw',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 89,
		),
		$client->updateChannelParticipant(
			via_chatlist : true,
			channel_id : -5339107747668297498,
			date : 97,
			actor_id : 1554142058740701610,
			user_id : 8710884734778792359,
			prev_participant : $client->channelParticipant(
				user_id : -2029556775100694344,
				date : 51,
				subscription_until_date : 51,
			),
			new_participant : $client->channelParticipant(
				user_id : 1879535515096649129,
				date : 22,
				subscription_until_date : 78,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'd8EuBlTJ6QcGaCVD',
				admin_id : 8583747092259545301,
				date : 12,
				start_date : 19,
				expire_date : 13,
				usage_limit : 95,
				usage : 32,
				requested : 76,
				subscription_expired : 54,
				title : 'hJwnLTQREmq4t3oc',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 22,
		),
		$client->updateBotStopped(
			user_id : -2696844490386098500,
			date : 42,
			stopped : $client->boolFalse(),
			qts : 82,
		),
		$client->updateGroupCallConnection(
			presentation : true,
			params : $client->dataJSON(
				data : 'x9WpiTNOqZtgHBlm',
			),
		),
		$client->updateBotCommands(
			peer : $client->peerUser(
				user_id : -3483364636426651136,
			),
			bot_id : 1595990768777261080,
			commands : array(
				$client->botCommand(
					command : 'dNuHi4meSqhVOCQj',
					description : 'IeTLZsPOYSijbDXW',
				),
			),
		),
		$client->updatePendingJoinRequests(
			peer : $client->peerUser(
				user_id : -1405728576081828644,
			),
			requests_pending : 15,
			recent_requesters : array(4186213447961964896),
		),
		$client->updateBotChatInviteRequester(
			peer : $client->peerUser(
				user_id : 55102120233985520,
			),
			date : 51,
			user_id : 6710565320654569131,
			about : 'yZrQqPNjA3opO0aB',
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'klGwLQCfK9yJzMbt',
				admin_id : 6844224701347762925,
				date : 79,
				start_date : 7,
				expire_date : 71,
				usage_limit : 64,
				usage : 68,
				requested : 25,
				subscription_expired : 74,
				title : 'qId710V4fzX8jBAk',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 39,
		),
		$client->updateMessageReactions(
			peer : $client->peerUser(
				user_id : 5638070139420598415,
			),
			msg_id : 68,
			top_msg_id : 63,
			saved_peer_id : $client->peerUser(
				user_id : 6514148412574139608,
			),
			reactions : $client->messageReactions(
				min : true,
				can_see_list : true,
				reactions_as_tags : true,
				results : array(
					$client->reactionCount(...),
				),
				recent_reactions : array(
					$client->messagePeerReaction(...),
				),
				top_reactors : array(
					$client->messageReactor(...),
				),
			),
		),
		$client->updateAttachMenuBots(),
		$client->updateWebViewResultSent(
			query_id : -7953466380984818933,
		),
		$client->updateBotMenuButton(
			bot_id : 3559521017788080455,
			button : $client->botMenuButtonDefault(),
		),
		$client->updateSavedRingtones(),
		$client->updateTranscribedAudio(
			pending : true,
			peer : $client->peerUser(
				user_id : 372064041822926104,
			),
			msg_id : 88,
			transcription_id : 1532641999892715521,
			text : 'f9l4HwoZmzpyUCQ6',
		),
		$client->updateReadFeaturedEmojiStickers(),
		$client->updateUserEmojiStatus(
			user_id : -3866922091552058713,
			emoji_status : $client->emojiStatusEmpty(),
		),
		$client->updateRecentEmojiStatuses(),
		$client->updateRecentReactions(),
		$client->updateMoveStickerSetToTop(
			masks : true,
			emojis : true,
			stickerset : 1137500237914781667,
		),
		$client->updateMessageExtendedMedia(
			peer : $client->peerUser(
				user_id : -3010581181269730876,
			),
			msg_id : 80,
			extended_media : array(
				$client->messageExtendedMediaPreview(
					w : 33,
					h : 16,
					thumb : $client->photoSizeEmpty(...),
					video_duration : 36,
				),
				$client->messageExtendedMedia(
					media : $client->messageMediaEmpty(...),
				),
			),
		),
		$client->updateChannelPinnedTopic(
			pinned : true,
			channel_id : -3244699464270210096,
			topic_id : 48,
		),
		$client->updateChannelPinnedTopics(
			channel_id : -4812547843491657755,
			order : array(65),
		),
		$client->updateUser(
			user_id : -7481686684772704077,
		),
		$client->updateAutoSaveSettings(),
		$client->updateStory(
			peer : $client->peerUser(
				user_id : 3175376530453669600,
			),
			story : $client->storyItemDeleted(
				id : 98,
			),
		),
		$client->updateReadStories(
			peer : $client->peerUser(
				user_id : 218339432012684618,
			),
			max_id : 16,
		),
		$client->updateStoryID(
			id : 26,
			random_id : 6583784615716319860,
		),
		$client->updateStoriesStealthMode(
			stealth_mode : $client->storiesStealthMode(
				active_until_date : 17,
				cooldown_until_date : 8,
			),
		),
		$client->updateSentStoryReaction(
			peer : $client->peerUser(
				user_id : 9205758665877040058,
			),
			story_id : 1,
			reaction : $client->reactionEmpty(),
		),
		$client->updateBotChatBoost(
			peer : $client->peerUser(
				user_id : 1759022424219037385,
			),
			boost : $client->boost(
				gift : true,
				giveaway : true,
				unclaimed : true,
				id : 'kPtDTXWFrIzNUpcv',
				user_id : 5664465199459285662,
				giveaway_msg_id : 88,
				date : 80,
				expires : 84,
				used_gift_slug : 'zSefoKVBar17NiWL',
				multiplier : 42,
				stars : -874560470782036554,
			),
			qts : 60,
		),
		$client->updateChannelViewForumAsMessages(
			channel_id : -4637687856787900048,
			enabled : $client->boolFalse(),
		),
		$client->updatePeerWallpaper(
			wallpaper_overridden : true,
			peer : $client->peerUser(
				user_id : 7838702284121855968,
			),
			wallpaper : $client->wallPaper(
				id : 2155822550827371510,
				creator : true,
				default : true,
				pattern : true,
				dark : true,
				access_hash : 5096132539744580117,
				slug : 'hr0MCjv3sz9ekFOb',
				document : $client->documentEmpty(...),
				settings : $client->wallPaperSettings(...),
			),
		),
		$client->updateBotMessageReaction(
			peer : $client->peerUser(
				user_id : 4132602340063537879,
			),
			msg_id : 73,
			date : 46,
			actor : $client->peerUser(
				user_id : -5347771658026287625,
			),
			old_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'ybgxWjqHelRdYKvZ',
				),
				$client->reactionCustomEmoji(
					document_id : 2010026656838979428,
				),
				$client->reactionPaid(),
			),
			new_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'tO53w1I6dBJmo4Zb',
				),
				$client->reactionCustomEmoji(
					document_id : -5574971981657527586,
				),
				$client->reactionPaid(),
			),
			qts : 50,
		),
		$client->updateBotMessageReactions(
			peer : $client->peerUser(
				user_id : -4770142516932901698,
			),
			msg_id : 12,
			date : 24,
			reactions : array(
				$client->reactionCount(
					chosen_order : 24,
					reaction : $client->reactionEmpty(...),
					count : 88,
				),
			),
			qts : 21,
		),
		$client->updateSavedDialogPinned(
			pinned : true,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
		),
		$client->updatePinnedSavedDialogs(
			order : array(
				$client->dialogPeer(
					peer : $client->peerUser(...),
				),
				$client->dialogPeerFolder(
					folder_id : 89,
				),
			),
		),
		$client->updateSavedReactionTags(),
		$client->updateSmsJob(
			job_id : 'Z5wltShPxW23A8Fy',
		),
		$client->updateQuickReplies(
			quick_replies : array(
				$client->quickReply(
					shortcut_id : 33,
					shortcut : 'AMNeBHQpbcdjziXu',
					top_message : 81,
					count : 72,
				),
			),
		),
		$client->updateNewQuickReply(
			quick_reply : $client->quickReply(
				shortcut_id : 40,
				shortcut : 'P7TYLWC9uRbBHpGy',
				top_message : 84,
				count : 77,
			),
		),
		$client->updateDeleteQuickReply(
			shortcut_id : 47,
		),
		$client->updateQuickReplyMessage(
			message : $client->messageEmpty(
				id : 64,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteQuickReplyMessages(
			shortcut_id : 89,
			messages : array(9),
		),
		$client->updateBotBusinessConnect(
			connection : $client->botBusinessConnection(
				disabled : true,
				connection_id : 'zPG3jie7pCI0lQsD',
				user_id : 5964165000587845431,
				dc_id : 29,
				date : 91,
				rights : $client->businessBotRights(...),
			),
			qts : 76,
		),
		$client->updateBotNewBusinessMessage(
			connection_id : 'kj4QRqOt81xEpVX7',
			message : $client->messageEmpty(
				id : 28,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 10,
				peer_id : $client->peerUser(...),
			),
			qts : 97,
		),
		$client->updateBotEditBusinessMessage(
			connection_id : 'FO8605rzbp1UMyvj',
			message : $client->messageEmpty(
				id : 41,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 56,
				peer_id : $client->peerUser(...),
			),
			qts : 89,
		),
		$client->updateBotDeleteBusinessMessage(
			connection_id : 'vYUtpJfmz2TGnZNS',
			peer : $client->peerUser(
				user_id : 6572630131132669960,
			),
			messages : array(40),
			qts : 11,
		),
		$client->updateNewStoryReaction(
			story_id : 54,
			peer : $client->peerUser(
				user_id : 7609361673684571247,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->updateStarsBalance(
			balance : $client->starsAmount(
				amount : -3195537907793486287,
				nanos : 94,
			),
		),
		$client->updateBusinessBotCallbackQuery(
			query_id : 1419040267643429930,
			user_id : 7013274700081621514,
			connection_id : 'IiFuGvRO75P8hcrT',
			message : $client->messageEmpty(
				id : 26,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 56,
				peer_id : $client->peerUser(...),
			),
			chat_instance : 1327772598114499503,
			data : '?K?f?LiveProto???',
		),
		$client->updateStarsRevenueStatus(
			peer : $client->peerUser(
				user_id : 9087914982913995397,
			),
			status : $client->starsRevenueStatus(
				withdrawal_enabled : true,
				current_balance : $client->starsAmount(...),
				available_balance : $client->starsAmount(...),
				overall_revenue : $client->starsAmount(...),
				next_withdrawal_at : 4,
			),
		),
		$client->updateBotPurchasedPaidMedia(
			user_id : 3553436089425370337,
			payload : 'Jc6DMqg4V8wpLu3O',
			qts : 60,
		),
		$client->updatePaidReactionPrivacy(
			private : $client->paidReactionPrivacyDefault(),
		),
		$client->updateSentPhoneCode(
			sent_code : $client->auth->sentCode(
				type : $client->auth->sentCodeTypeApp(...),
				phone_code_hash : '+1234567890',
				next_type : $client->auth->codeTypeSms(...),
				timeout : 82,
			),
		),
		$client->updateGroupCallChainBlocks(
			call : $client->inputGroupCall(
				id : -8282169291841617316,
				access_hash : -8193928653743060449,
			),
			sub_chain_id : 13,
			blocks : array('d!P?bLiveProto$	??'),
			next_offset : 49,
		),
		$client->updateReadMonoForumInbox(
			channel_id : -6543064199674361481,
			saved_peer_id : $client->peerUser(
				user_id : 5917874695958022775,
			),
			read_max_id : 73,
		),
		$client->updateReadMonoForumOutbox(
			channel_id : -8267166032360243299,
			saved_peer_id : $client->peerUser(
				user_id : -3240639800958508251,
			),
			read_max_id : 57,
		),
		$client->updateMonoForumNoPaidException(
			exception : true,
			channel_id : -6587333171372206529,
			saved_peer_id : $client->peerUser(
				user_id : -5501427913777912445,
			),
		),
	),
	users : array(
		$client->userEmpty(
			id : -3755942058917596678,
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
			id : -1962873028539941866,
			access_hash : 1021366965978388764,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 90,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'qUDeZs3JKontcrxT',
					reason : 'j9M6zoPw3mvShlr7',
					text : 'FlnTGs7ILXvj1Sdt',
				),
			),
			bot_inline_placeholder : 'hZTMQV1jkta9s25F',
			lang_code : '2xD670Uzfi5KaCXe',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 44,
			color : $client->peerColor(
				color : 65,
				background_emoji_id : -476327525325351493,
			),
			profile_color : $client->peerColor(
				color : 9,
				background_emoji_id : -4592876039827390137,
			),
			bot_active_users : 66,
			bot_verification_icon : 6066308321277661830,
			send_paid_messages_stars : -4898063601450057212,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -5748213901380596649,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -2004200452030149583,
			title : 'lUHWYkruINjtenv0',
			photo : $client->chatPhotoEmpty(),
			participants_count : 47,
			date : 51,
			version : 25,
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
				until_date : 61,
			),
		),
		$client->chatForbidden(
			id : 3985128611175012767,
			title : 'co1wZetvBsQT0lhy',
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
			id : -8148002706585337670,
			access_hash : -2766940433354626986,
			title : 'RNKFyzfXGL2VUc7Z',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 23,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'y6CNH95mxRl7OvrW',
					reason : 'HTRVnOidLJtM81s9',
					text : 'Wlhc8FdXfnHgtv4B',
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
				until_date : 63,
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
				until_date : 7,
			),
			participants_count : 64,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 61,
			color : $client->peerColor(
				color : 88,
				background_emoji_id : 2175817943237159893,
			),
			profile_color : $client->peerColor(
				color : 10,
				background_emoji_id : -2576212553807385611,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 91,
			subscription_until_date : 16,
			bot_verification_icon : 5360254672039697288,
			send_paid_messages_stars : -3165611024108464161,
			linked_monoforum_id : -2872297812825669510,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 8304074362615599026,
			access_hash : 3925292098392070595,
			title : 'X6n1H4sgIxc7D5Ua',
			until_date : 25,
		),
	),
	date : 78,
	seq_start : 92,
	seq : 81,
);
```