# updates

**Description** : *Full constructor of updates*

**Layer** : 211

```tl
updates#74ae4240 updates:Vector<Update> users:Vector<User> chats:Vector<Chat> date:int seq:int = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>updates</mark> | [`Vector<Update>`](type/Update) | List of updates |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of users mentioned in updates |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | List of chats mentioned in updates |
| <mark>date</mark> | [`int`](type/int) | Current date |
| <mark>seq</mark> | [`int`](type/int) | Total number of sent updates |

---

## Type

[Updates](type/Updates)

---

## Example

```php
$updates = $client->updates(
	updates : array(
		$client->updateNewMessage(
			message : $client->messageEmpty(
				id : 40,
				peer_id : $client->peerUser(...),
			),
			pts : 27,
			pts_count : 39,
		),
		$client->updateMessageID(
			id : 17,
			random_id : 3278388830208732000,
		),
		$client->updateDeleteMessages(
			messages : array(85),
			pts : 23,
			pts_count : 26,
		),
		$client->updateUserTyping(
			user_id : -2157396260757849408,
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatUserTyping(
			chat_id : 6420566223868097182,
			from_id : $client->peerUser(
				user_id : 7215062354628748358,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatParticipants(
			participants : $client->chatParticipantsForbidden(
				chat_id : -1239492284217501999,
				self_participant : $client->chatParticipant(...),
			),
		),
		$client->updateUserStatus(
			user_id : 3846270868731333307,
			status : $client->userStatusEmpty(),
		),
		$client->updateUserName(
			user_id : 4338637693326927611,
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
			hash : -3511404880902411222,
			date : 80,
			device : '93Hkh8uVYrUlZbR2',
			location : 'tonxrq1b2AWS6h9y',
		),
		$client->updateNewEncryptedMessage(
			message : $client->encryptedMessage(
				random_id : 4440829472250956915,
				chat_id : 70,
				date : 4,
				bytes : '??3w?LiveProtoC?8?',
				file : $client->encryptedFileEmpty(...),
			),
			qts : 17,
		),
		$client->updateEncryptedChatTyping(
			chat_id : 76,
		),
		$client->updateEncryption(
			chat : $client->encryptedChatEmpty(
				id : 88,
			),
			date : 20,
		),
		$client->updateEncryptedMessagesRead(
			chat_id : 99,
			max_date : 73,
			date : 82,
		),
		$client->updateChatParticipantAdd(
			chat_id : 6328109481210577654,
			user_id : 7784572618396319108,
			inviter_id : -5147817746426322929,
			date : 80,
			version : 66,
		),
		$client->updateChatParticipantDelete(
			chat_id : -1844439856549870236,
			user_id : 4355870695964999731,
			version : 49,
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
					id : 20,
					ip_address : '127.0.0.1',
					port : 60,
					secret : '|?A?LiveProto?u?',
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
				mute_until : 80,
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
			inbox_date : 70,
			type : 'UgtCcyr06bHfWQ25',
			message : 'wIkHfyBoXDxMY2Wr',
			media : $client->messageMediaEmpty(),
			entities : array(
				$client->messageEntityUnknown(
					offset : 85,
					length : 90,
				),
				$client->messageEntityMention(
					offset : 31,
					length : 4,
				),
				$client->messageEntityHashtag(
					offset : 13,
					length : 44,
				),
				$client->messageEntityBotCommand(
					offset : 54,
					length : 37,
				),
				$client->messageEntityUrl(
					offset : 37,
					length : 58,
				),
				$client->messageEntityEmail(
					offset : 30,
					length : 16,
				),
				$client->messageEntityBold(
					offset : 54,
					length : 81,
				),
				$client->messageEntityItalic(
					offset : 94,
					length : 61,
				),
				$client->messageEntityCode(
					offset : 99,
					length : 48,
				),
				$client->messageEntityPre(
					offset : 85,
					length : 53,
					language : '3XGnzUEaLxls1m8I',
				),
				$client->messageEntityTextUrl(
					offset : 58,
					length : 6,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 64,
					length : 39,
					user_id : -1143244155845773800,
				),
				$client->inputMessageEntityMentionName(
					offset : 14,
					length : 100,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 25,
					length : 63,
				),
				$client->messageEntityCashtag(
					offset : 8,
					length : 13,
				),
				$client->messageEntityUnderline(
					offset : 29,
					length : 8,
				),
				$client->messageEntityStrike(
					offset : 98,
					length : 97,
				),
				$client->messageEntityBankCard(
					offset : 54,
					length : 96,
				),
				$client->messageEntitySpoiler(
					offset : 71,
					length : 81,
				),
				$client->messageEntityCustomEmoji(
					offset : 49,
					length : 30,
					document_id : -1797421079877485239,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 16,
					length : 2,
				),
			),
		),
		$client->updatePrivacy(
			key : $client->privacyKeyStatusTimestamp(),
			rules : array(
				$client->privacyValueAllowContacts(),
				$client->privacyValueAllowAll(),
				$client->privacyValueAllowUsers(
					users : array(2929520784453945888),
				),
				$client->privacyValueDisallowContacts(),
				$client->privacyValueDisallowAll(),
				$client->privacyValueDisallowUsers(
					users : array(2580027424890487856),
				),
				$client->privacyValueAllowChatParticipants(
					chats : array(-316250193577185681),
				),
				$client->privacyValueDisallowChatParticipants(
					chats : array(3539249438265710058),
				),
				$client->privacyValueAllowCloseFriends(),
				$client->privacyValueAllowPremium(),
				$client->privacyValueAllowBots(),
				$client->privacyValueDisallowBots(),
			),
		),
		$client->updateUserPhone(
			user_id : -1382142296175152088,
			phone : '+1234567890',
		),
		$client->updateReadHistoryInbox(
			folder_id : 57,
			peer : $client->peerUser(
				user_id : 4118602050089487907,
			),
			max_id : 87,
			still_unread_count : 82,
			pts : 10,
			pts_count : 62,
		),
		$client->updateReadHistoryOutbox(
			peer : $client->peerUser(
				user_id : 2767228965852112358,
			),
			max_id : 74,
			pts : 59,
			pts_count : 41,
		),
		$client->updateWebPage(
			webpage : $client->webPageEmpty(
				id : 1548370046123933209,
				url : 'https://docs.liveproto.dev',
			),
			pts : 100,
			pts_count : 11,
		),
		$client->updateReadMessagesContents(
			messages : array(49),
			pts : 70,
			pts_count : 13,
			date : 44,
		),
		$client->updateChannelTooLong(
			channel_id : -5958422704257742610,
			pts : 17,
		),
		$client->updateChannel(
			channel_id : 9063936496862811369,
		),
		$client->updateNewChannelMessage(
			message : $client->messageEmpty(
				id : 87,
				peer_id : $client->peerUser(...),
			),
			pts : 0,
			pts_count : 17,
		),
		$client->updateReadChannelInbox(
			folder_id : 64,
			channel_id : 6964034198687233062,
			max_id : 36,
			still_unread_count : 36,
			pts : 96,
		),
		$client->updateDeleteChannelMessages(
			channel_id : -7629696083593986059,
			messages : array(91),
			pts : 64,
			pts_count : 12,
		),
		$client->updateChannelMessageViews(
			channel_id : -8600292350407662077,
			id : 36,
			views : 4,
		),
		$client->updateChatParticipantAdmin(
			chat_id : -3700849800728147739,
			user_id : 5555288404997741939,
			is_admin : $client->boolFalse(),
			version : 30,
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
			order : array(-7157659757632549560),
		),
		$client->updateStickerSets(
			masks : true,
			emojis : true,
		),
		$client->updateSavedGifs(),
		$client->updateBotInlineQuery(
			query_id : -7976331516311261496,
			user_id : 5678031308925897228,
			query : '8eXwdxOFUG7arbAN',
			geo : $client->geoPointEmpty(),
			peer_type : $client->inlineQueryPeerTypeSameBotPM(),
			offset : 'JKi7bNfyA6aCEmDO',
		),
		$client->updateBotInlineSend(
			user_id : -8174147932581413739,
			query : 'iw3cQXo2SDPnubNA',
			geo : $client->geoPointEmpty(),
			id : 'MtvsPXxQi26VKkEl',
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 65,
				id : 6940277331157752201,
				access_hash : -969113375344241327,
			),
		),
		$client->updateEditChannelMessage(
			message : $client->messageEmpty(
				id : 23,
				peer_id : $client->peerUser(...),
			),
			pts : 85,
			pts_count : 17,
		),
		$client->updateBotCallbackQuery(
			query_id : -7921326904836737495,
			user_id : 976458856246591889,
			peer : $client->peerUser(
				user_id : -1060677143397216649,
			),
			msg_id : 47,
			chat_instance : -4480294533308018002,
			data : '?[??LiveProto?W?',
			game_short_name : 'QLqWXCfigTD9ajMH',
		),
		$client->updateEditMessage(
			message : $client->messageEmpty(
				id : 56,
				peer_id : $client->peerUser(...),
			),
			pts : 37,
			pts_count : 77,
		),
		$client->updateInlineBotCallbackQuery(
			query_id : -1850068758251586093,
			user_id : -6560507301698556452,
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 4,
				id : -129649720029914603,
				access_hash : -6911067862901636263,
			),
			chat_instance : -7945491842896265084,
			data : '`??,LiveProtoSZ	?I',
			game_short_name : 'Ic3LbjPfHa7Qk6y0',
		),
		$client->updateReadChannelOutbox(
			channel_id : -3288988461862245862,
			max_id : 30,
		),
		$client->updateDraftMessage(
			peer : $client->peerUser(
				user_id : 8550781145629578551,
			),
			top_msg_id : 95,
			saved_peer_id : $client->peerUser(
				user_id : 3048582381669282277,
			),
			draft : $client->draftMessageEmpty(
				date : 40,
			),
		),
		$client->updateReadFeaturedStickers(),
		$client->updateRecentStickers(),
		$client->updateConfig(),
		$client->updatePtsChanged(),
		$client->updateChannelWebPage(
			channel_id : -9042444655479366747,
			webpage : $client->webPageEmpty(
				id : 5873971507778916253,
				url : 'https://docs.liveproto.dev',
			),
			pts : 41,
			pts_count : 91,
		),
		$client->updateDialogPinned(
			pinned : true,
			folder_id : 69,
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
					folder_id : 14,
				),
			),
		),
		$client->updateBotWebhookJSON(
			data : $client->dataJSON(
				data : 'cPdKxNQUzS6JroAg',
			),
		),
		$client->updateBotWebhookJSONQuery(
			query_id : -4434348933010980040,
			data : $client->dataJSON(
				data : 'fFQn2P9myH5VZYsa',
			),
			timeout : 51,
		),
		$client->updateBotShippingQuery(
			query_id : -8200385193563996555,
			user_id : 6926703081850938777,
			payload : '??OB?LiveProtoε2??',
			shipping_address : $client->postAddress(
				street_line1 : 'YiaUXIckDHubW9BQ',
				street_line2 : '7QWb2fkKNInHagOZ',
				city : 'twDqQWYzIpFeSlXo',
				state : 'uqxcGr6o2Mdv5efW',
				country_iso2 : 'CHfK6nQydWStI5Em',
				post_code : '7HpWRbYmFoiCkXMT',
			),
		),
		$client->updateBotPrecheckoutQuery(
			query_id : -8510125110370040287,
			user_id : -847530805587053567,
			payload : 'B?Q?BLiveProto????',
			info : $client->paymentRequestedInfo(
				name : 'Ee8g9WmUIflB7YoZ',
				phone : '+1234567890',
				email : 'reply@liveproto.dev',
				shipping_address : $client->postAddress(...),
			),
			shipping_option_id : 'b0BlypNI5t7J8oLi',
			currency : 'faiL3uHgSxqpyhto',
			total_amount : 3842177575907577732,
		),
		$client->updatePhoneCall(
			phone_call : $client->phoneCallEmpty(
				id : 7088889717150563890,
			),
		),
		$client->updateLangPackTooLong(
			lang_code : '3EwPkU2CQf5eioD0',
		),
		$client->updateLangPack(
			difference : $client->langPackDifference(
				lang_code : 'WPa6McXZJOKvyDrH',
				from_version : 11,
				version : 73,
				strings : array(
					$client->langPackString(...),
					$client->langPackStringPluralized(...),
					$client->langPackStringDeleted(...),
				),
			),
		),
		$client->updateFavedStickers(),
		$client->updateChannelReadMessagesContents(
			channel_id : -3525272461923131374,
			top_msg_id : 44,
			saved_peer_id : $client->peerUser(
				user_id : -1945525537818059281,
			),
			messages : array(6),
		),
		$client->updateContactsReset(),
		$client->updateChannelAvailableMessages(
			channel_id : 7212753067884346400,
			available_min_id : 64,
		),
		$client->updateDialogUnreadMark(
			unread : true,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
			saved_peer_id : $client->peerUser(
				user_id : -4168417283830293408,
			),
		),
		$client->updateMessagePoll(
			poll_id : 826419813929285896,
			poll : $client->poll(
				id : 4967511834445584887,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 91,
				close_date : 48,
			),
			results : $client->pollResults(
				min : true,
				results : array(
					$client->pollAnswerVoters(...),
				),
				total_voters : 14,
				recent_voters : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				solution : 'mTDBVx7LoWvJYzuF',
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
				user_id : -2856796243887644322,
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
				until_date : 8,
			),
			version : 14,
		),
		$client->updateFolderPeers(
			folder_peers : array(
				$client->folderPeer(
					peer : $client->peerUser(...),
					folder_id : 13,
				),
			),
			pts : 37,
			pts_count : 22,
		),
		$client->updatePeerSettings(
			peer : $client->peerUser(
				user_id : 6831534260291043931,
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
				geo_distance : 7,
				request_chat_title : 'Bil1O9j6ETd720bw',
				request_chat_date : 48,
				business_bot_id : 6578002711835003407,
				business_bot_manage_url : 'https://docs.liveproto.dev',
				charge_paid_message_stars : -3376999030550209552,
				registration_month : 'mBIL5AZWNPOY4FrM',
				phone_country : '+1234567890',
				name_change_date : 54,
				photo_change_date : 26,
			),
		),
		$client->updatePeerLocated(
			peers : array(
				$client->peerLocated(
					peer : $client->peerUser(...),
					expires : 4,
					distance : 80,
				),
				$client->peerSelfLocated(
					expires : 5,
				),
			),
		),
		$client->updateNewScheduledMessage(
			message : $client->messageEmpty(
				id : 85,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteScheduledMessages(
			peer : $client->peerUser(
				user_id : -1001105826272667723,
			),
			messages : array(67),
			sent_messages : array(37),
		),
		$client->updateTheme(
			theme : $client->theme(
				creator : true,
				default : true,
				for_chat : true,
				id : 6252633942745727550,
				access_hash : 7703658403234836033,
				slug : 'JIQb1ca5ihV60DBC',
				title : 'sGocOZLKI2v6fCR0',
				document : $client->documentEmpty(...),
				settings : array(
					$client->themeSettings(...),
				),
				emoticon : 'K6Mk1tWZm3Ipzyav',
				installs_count : 50,
			),
		),
		$client->updateGeoLiveViewed(
			peer : $client->peerUser(
				user_id : 8567485679973268796,
			),
			msg_id : 74,
		),
		$client->updateLoginToken(),
		$client->updateMessagePollVote(
			poll_id : -7052675163102810257,
			peer : $client->peerUser(
				user_id : 4380131371242690936,
			),
			options : array('ߺ??tLiveProto?J7??'),
			qts : 52,
		),
		$client->updateDialogFilter(
			id : 79,
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
				id : 54,
				title : $client->textWithEntities(...),
				emoticon : 'E6vuyxaQZbnhJH8O',
				color : 63,
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
			order : array(66),
		),
		$client->updateDialogFilters(),
		$client->updatePhoneCallSignalingData(
			phone_call_id : -5500828579242418095,
			data : '?Z' . "\0" . '=LiveProto9?#?',
		),
		$client->updateChannelMessageForwards(
			channel_id : 6906679436822461759,
			id : 3,
			forwards : 96,
		),
		$client->updateReadChannelDiscussionInbox(
			channel_id : 4864403879645664841,
			top_msg_id : 96,
			read_max_id : 38,
			broadcast_id : -1521978990561149565,
			broadcast_post : 7,
		),
		$client->updateReadChannelDiscussionOutbox(
			channel_id : 3719541729878146805,
			top_msg_id : 24,
			read_max_id : 3,
		),
		$client->updatePeerBlocked(
			blocked : true,
			blocked_my_stories_from : true,
			peer_id : $client->peerUser(
				user_id : -5937762290401769551,
			),
		),
		$client->updateChannelUserTyping(
			channel_id : -1814686575929380869,
			top_msg_id : 15,
			from_id : $client->peerUser(
				user_id : 3443042729235775274,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updatePinnedMessages(
			pinned : true,
			peer : $client->peerUser(
				user_id : 3516169737332045765,
			),
			messages : array(61),
			pts : 66,
			pts_count : 46,
		),
		$client->updatePinnedChannelMessages(
			pinned : true,
			channel_id : 7503564227326943162,
			messages : array(12),
			pts : 32,
			pts_count : 39,
		),
		$client->updateChat(
			chat_id : -8941156721036858887,
		),
		$client->updateGroupCallParticipants(
			call : $client->inputGroupCall(
				id : 3232965714169848053,
				access_hash : -774422935351347937,
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
					date : 45,
					active_date : 4,
					source : 37,
					volume : 28,
					about : '7H1lyTjbdkm5aX3g',
					raise_hand_rating : 5492502778007433981,
					video : $client->groupCallParticipantVideo(...),
					presentation : $client->groupCallParticipantVideo(...),
				),
			),
			version : 57,
		),
		$client->updateGroupCall(
			chat_id : 9178910185346433772,
			call : $client->groupCallDiscarded(
				id : 710927125408172399,
				access_hash : 4778076288221498055,
				duration : 61,
			),
		),
		$client->updatePeerHistoryTTL(
			peer : $client->peerUser(
				user_id : 1497991971915346905,
			),
			ttl_period : 12,
		),
		$client->updateChatParticipant(
			chat_id : 8359991191786787118,
			date : 16,
			actor_id : -1865763209502155976,
			user_id : 8003693599148344593,
			prev_participant : $client->chatParticipant(
				user_id : 5276698819589590794,
				inviter_id : -8044966844257762590,
				date : 86,
			),
			new_participant : $client->chatParticipant(
				user_id : -9001421267332227128,
				inviter_id : -4765883041378585499,
				date : 29,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'plsSz1ebENCG5hF9',
				admin_id : -2771275179696739833,
				date : 64,
				start_date : 12,
				expire_date : 25,
				usage_limit : 85,
				usage : 39,
				requested : 85,
				subscription_expired : 84,
				title : 'ClVs9y3F42YgunQX',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 75,
		),
		$client->updateChannelParticipant(
			via_chatlist : true,
			channel_id : 1336246413202900894,
			date : 21,
			actor_id : 826251397791788609,
			user_id : 8577354600246369945,
			prev_participant : $client->channelParticipant(
				user_id : 8317164738403090255,
				date : 74,
				subscription_until_date : 56,
			),
			new_participant : $client->channelParticipant(
				user_id : -1226814603416843707,
				date : 51,
				subscription_until_date : 56,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'witSpgPEOUMJaCbf',
				admin_id : 5031303383024165935,
				date : 82,
				start_date : 56,
				expire_date : 48,
				usage_limit : 34,
				usage : 19,
				requested : 66,
				subscription_expired : 58,
				title : '0PnIbRysQz2CMmxK',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 34,
		),
		$client->updateBotStopped(
			user_id : 3488155042425495603,
			date : 90,
			stopped : $client->boolFalse(),
			qts : 14,
		),
		$client->updateGroupCallConnection(
			presentation : true,
			params : $client->dataJSON(
				data : 'hugnrNmXc839a0Fe',
			),
		),
		$client->updateBotCommands(
			peer : $client->peerUser(
				user_id : 504403489724073500,
			),
			bot_id : -5890526065479264775,
			commands : array(
				$client->botCommand(
					command : 'UFWxnce32SyRMJjD',
					description : 'wFSoxepYgl3OHGXJ',
				),
			),
		),
		$client->updatePendingJoinRequests(
			peer : $client->peerUser(
				user_id : -150816835893217103,
			),
			requests_pending : 39,
			recent_requesters : array(3228661533845379795),
		),
		$client->updateBotChatInviteRequester(
			peer : $client->peerUser(
				user_id : 3903850163199887026,
			),
			date : 44,
			user_id : 882774517660583499,
			about : '9owAmg4GkbHWT0Kp',
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'OWavjTIz9rew8Mh6',
				admin_id : -4717705590525999096,
				date : 52,
				start_date : 59,
				expire_date : 9,
				usage_limit : 95,
				usage : 34,
				requested : 47,
				subscription_expired : 81,
				title : 'Z3NK6qc82Ra7SuXk',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 33,
		),
		$client->updateMessageReactions(
			peer : $client->peerUser(
				user_id : -3238690043307901023,
			),
			msg_id : 27,
			top_msg_id : 53,
			saved_peer_id : $client->peerUser(
				user_id : 131290695266086403,
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
			query_id : 4550179048002903137,
		),
		$client->updateBotMenuButton(
			bot_id : 6002819430068988809,
			button : $client->botMenuButtonDefault(),
		),
		$client->updateSavedRingtones(),
		$client->updateTranscribedAudio(
			pending : true,
			peer : $client->peerUser(
				user_id : -3079383332371061400,
			),
			msg_id : 21,
			transcription_id : -9110680811697484713,
			text : '2DhBpYmELe6cfNtg',
		),
		$client->updateReadFeaturedEmojiStickers(),
		$client->updateUserEmojiStatus(
			user_id : -7851815677772356902,
			emoji_status : $client->emojiStatusEmpty(),
		),
		$client->updateRecentEmojiStatuses(),
		$client->updateRecentReactions(),
		$client->updateMoveStickerSetToTop(
			masks : true,
			emojis : true,
			stickerset : 7111649663205276993,
		),
		$client->updateMessageExtendedMedia(
			peer : $client->peerUser(
				user_id : -8319046920425997409,
			),
			msg_id : 79,
			extended_media : array(
				$client->messageExtendedMediaPreview(
					w : 89,
					h : 15,
					thumb : $client->photoSizeEmpty(...),
					video_duration : 45,
				),
				$client->messageExtendedMedia(
					media : $client->messageMediaEmpty(...),
				),
			),
		),
		$client->updateChannelPinnedTopic(
			pinned : true,
			channel_id : -6418415993545935629,
			topic_id : 31,
		),
		$client->updateChannelPinnedTopics(
			channel_id : 333331427823069481,
			order : array(64),
		),
		$client->updateUser(
			user_id : 1808405667160937013,
		),
		$client->updateAutoSaveSettings(),
		$client->updateStory(
			peer : $client->peerUser(
				user_id : -6508081415776053272,
			),
			story : $client->storyItemDeleted(
				id : 24,
			),
		),
		$client->updateReadStories(
			peer : $client->peerUser(
				user_id : 4766579799805745862,
			),
			max_id : 77,
		),
		$client->updateStoryID(
			id : 83,
			random_id : -3658888507841451556,
		),
		$client->updateStoriesStealthMode(
			stealth_mode : $client->storiesStealthMode(
				active_until_date : 30,
				cooldown_until_date : 19,
			),
		),
		$client->updateSentStoryReaction(
			peer : $client->peerUser(
				user_id : 1525647554973526433,
			),
			story_id : 97,
			reaction : $client->reactionEmpty(),
		),
		$client->updateBotChatBoost(
			peer : $client->peerUser(
				user_id : 5943501011064043948,
			),
			boost : $client->boost(
				gift : true,
				giveaway : true,
				unclaimed : true,
				id : 'XOq6Y3w1cCSnQmkM',
				user_id : -5905700017620115734,
				giveaway_msg_id : 37,
				date : 37,
				expires : 66,
				used_gift_slug : 'BnU6Lm0AjI85iOSg',
				multiplier : 83,
				stars : 8917749895084491411,
			),
			qts : 75,
		),
		$client->updateChannelViewForumAsMessages(
			channel_id : 6786267544247188720,
			enabled : $client->boolFalse(),
		),
		$client->updatePeerWallpaper(
			wallpaper_overridden : true,
			peer : $client->peerUser(
				user_id : -1784728188103570534,
			),
			wallpaper : $client->wallPaper(
				id : 3114970112661068565,
				creator : true,
				default : true,
				pattern : true,
				dark : true,
				access_hash : -1918521631613516628,
				slug : '6eMJilbXsR8Gcxtz',
				document : $client->documentEmpty(...),
				settings : $client->wallPaperSettings(...),
			),
		),
		$client->updateBotMessageReaction(
			peer : $client->peerUser(
				user_id : -6824676140031227911,
			),
			msg_id : 68,
			date : 86,
			actor : $client->peerUser(
				user_id : 4912989176284263295,
			),
			old_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'fvjzYoSws5UKmQk2',
				),
				$client->reactionCustomEmoji(
					document_id : -6625394799789723007,
				),
				$client->reactionPaid(),
			),
			new_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'UevHp9NQZEY2uD4S',
				),
				$client->reactionCustomEmoji(
					document_id : -5261390434378529840,
				),
				$client->reactionPaid(),
			),
			qts : 70,
		),
		$client->updateBotMessageReactions(
			peer : $client->peerUser(
				user_id : 6181501777460823380,
			),
			msg_id : 12,
			date : 89,
			reactions : array(
				$client->reactionCount(
					chosen_order : 7,
					reaction : $client->reactionEmpty(...),
					count : 96,
				),
			),
			qts : 1,
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
					folder_id : 100,
				),
			),
		),
		$client->updateSavedReactionTags(),
		$client->updateSmsJob(
			job_id : 'yQKsHEl3BUoCMDiZ',
		),
		$client->updateQuickReplies(
			quick_replies : array(
				$client->quickReply(
					shortcut_id : 100,
					shortcut : 'cYUOVP1NlpAvtRsf',
					top_message : 9,
					count : 62,
				),
			),
		),
		$client->updateNewQuickReply(
			quick_reply : $client->quickReply(
				shortcut_id : 90,
				shortcut : '4VvorWAaO7JMPUwy',
				top_message : 39,
				count : 25,
			),
		),
		$client->updateDeleteQuickReply(
			shortcut_id : 92,
		),
		$client->updateQuickReplyMessage(
			message : $client->messageEmpty(
				id : 86,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteQuickReplyMessages(
			shortcut_id : 53,
			messages : array(95),
		),
		$client->updateBotBusinessConnect(
			connection : $client->botBusinessConnection(
				disabled : true,
				connection_id : 'tWSBGYQZldh81NMU',
				user_id : 7078650288113375362,
				dc_id : 12,
				date : 100,
				rights : $client->businessBotRights(...),
			),
			qts : 92,
		),
		$client->updateBotNewBusinessMessage(
			connection_id : 'Pjl25oCOK1dRZmcG',
			message : $client->messageEmpty(
				id : 51,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 98,
				peer_id : $client->peerUser(...),
			),
			qts : 82,
		),
		$client->updateBotEditBusinessMessage(
			connection_id : 'S2O4JNEaBFUfoIgZ',
			message : $client->messageEmpty(
				id : 91,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 93,
				peer_id : $client->peerUser(...),
			),
			qts : 96,
		),
		$client->updateBotDeleteBusinessMessage(
			connection_id : 'mUjXCwYxWKLIi0gk',
			peer : $client->peerUser(
				user_id : 1888233169838937207,
			),
			messages : array(51),
			qts : 85,
		),
		$client->updateNewStoryReaction(
			story_id : 92,
			peer : $client->peerUser(
				user_id : -2210155044857260636,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->updateStarsBalance(
			balance : $client->starsAmount(
				amount : 7096173588651290203,
				nanos : 61,
			),
		),
		$client->updateBusinessBotCallbackQuery(
			query_id : -3632549004537598230,
			user_id : -5031775075761955408,
			connection_id : 'dfqau54bzyvMQFWr',
			message : $client->messageEmpty(
				id : 82,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 83,
				peer_id : $client->peerUser(...),
			),
			chat_instance : 2197658105309819222,
			data : '?G?#?LiveProto??.',
		),
		$client->updateStarsRevenueStatus(
			peer : $client->peerUser(
				user_id : -7858232919827236235,
			),
			status : $client->starsRevenueStatus(
				withdrawal_enabled : true,
				current_balance : $client->starsAmount(...),
				available_balance : $client->starsAmount(...),
				overall_revenue : $client->starsAmount(...),
				next_withdrawal_at : 11,
			),
		),
		$client->updateBotPurchasedPaidMedia(
			user_id : 7163541496120698094,
			payload : 'dP1pN40VWcxoBm5u',
			qts : 24,
		),
		$client->updatePaidReactionPrivacy(
			private : $client->paidReactionPrivacyDefault(),
		),
		$client->updateSentPhoneCode(
			sent_code : $client->auth->sentCode(
				type : $client->auth->sentCodeTypeApp(...),
				phone_code_hash : '+1234567890',
				next_type : $client->auth->codeTypeSms(...),
				timeout : 91,
			),
		),
		$client->updateGroupCallChainBlocks(
			call : $client->inputGroupCall(
				id : -2753305962347196740,
				access_hash : -9213285525283110387,
			),
			sub_chain_id : 97,
			blocks : array('???,JLiveProtoǸ?d'),
			next_offset : 44,
		),
		$client->updateReadMonoForumInbox(
			channel_id : 3025537559040604324,
			saved_peer_id : $client->peerUser(
				user_id : -1153642121526690585,
			),
			read_max_id : 92,
		),
		$client->updateReadMonoForumOutbox(
			channel_id : 1855427185133171895,
			saved_peer_id : $client->peerUser(
				user_id : 7331033432392159250,
			),
			read_max_id : 40,
		),
		$client->updateMonoForumNoPaidException(
			exception : true,
			channel_id : 5513207456092872749,
			saved_peer_id : $client->peerUser(
				user_id : -1389436656683570340,
			),
		),
	),
	users : array(
		$client->userEmpty(
			id : 1120573886701902781,
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
			id : 513885556768037020,
			access_hash : 3640841712121077947,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 10,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'o0BY1sAqKZNb8Pkx',
					reason : 'lJYMI71HABbGVNK9',
					text : 'kWwy5DYRud1egsSa',
				),
			),
			bot_inline_placeholder : '0FjyAzboqeKBIPmR',
			lang_code : 'RurewD98JlH57Usm',
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
				color : 14,
				background_emoji_id : 3907211204735444713,
			),
			profile_color : $client->peerColor(
				color : 84,
				background_emoji_id : 5724340309080206963,
			),
			bot_active_users : 74,
			bot_verification_icon : 3945777383280666302,
			send_paid_messages_stars : 5969331533188242202,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 8798138818894792289,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 3826675381209284834,
			title : 'oUsdH6DITy1nFuEh',
			photo : $client->chatPhotoEmpty(),
			participants_count : 18,
			date : 42,
			version : 86,
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
				until_date : 14,
			),
		),
		$client->chatForbidden(
			id : -4548932989474278995,
			title : 'Gi6E7udsVlz1ZWR4',
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
			id : -5975202459543263548,
			access_hash : -8368033922083444112,
			title : 'rTLP1Nn7wjEkCSaf',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 23,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'tnVXWhIPJBHSAsco',
					reason : 'PCMV0czD2gr1uTOZ',
					text : '9ovJMQaBDmYdyOzc',
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
				until_date : 48,
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
				until_date : 100,
			),
			participants_count : 34,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 3,
			color : $client->peerColor(
				color : 89,
				background_emoji_id : 359124152107622817,
			),
			profile_color : $client->peerColor(
				color : 43,
				background_emoji_id : -8981607687332956827,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 70,
			subscription_until_date : 47,
			bot_verification_icon : -7275961767475387068,
			send_paid_messages_stars : 429588696798235360,
			linked_monoforum_id : -3554201165434257908,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -8915589072179994886,
			access_hash : 5551367070725872219,
			title : '0Hlxip6U2XMJ9eEh',
			until_date : 54,
		),
	),
	date : 2,
	seq : 89,
);
```