# updates.difference

**Description** : *Full list of occurred events*

**Layer** : 211

```tl
updates.difference#f49ca0 new_messages:Vector<Message> new_encrypted_messages:Vector<EncryptedMessage> other_updates:Vector<Update> chats:Vector<Chat> users:Vector<User> state:updates.State = updates.Difference;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>new_messages</mark> | [`Vector<Message>`](type/Message) | List of new messages |
| <mark>new_encrypted_messages</mark> | [`Vector<EncryptedMessage>`](type/EncryptedMessage) | List of new encrypted secret chat messages |
| <mark>other_updates</mark> | [`Vector<Update>`](type/Update) | List of updates |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | List of chats mentioned in events |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of users mentioned in events |
| <mark>state</mark> | [`updates.State`](type/updates.State) | Current state |

---

## Type

[updates.Difference](type/updates.Difference)

---

## Example

```php
$updatesDifference = $client->updates->difference(
	new_messages : array(
		$client->messageEmpty(
			id : 92,
			peer_id : $client->peerUser(
				user_id : 2003693839855118144,
			),
		),
		$client->message(
			out : true,
			mentioned : true,
			media_unread : true,
			silent : true,
			post : true,
			from_scheduled : true,
			legacy : true,
			edit_hide : true,
			pinned : true,
			noforwards : true,
			invert_media : true,
			offline : true,
			video_processing_pending : true,
			paid_suggested_post_stars : true,
			paid_suggested_post_ton : true,
			id : 31,
			from_id : $client->peerUser(
				user_id : -7047996121448942506,
			),
			from_boosts_applied : 64,
			peer_id : $client->peerUser(
				user_id : -9196323339748212535,
			),
			saved_peer_id : $client->peerUser(
				user_id : -4864697584401346267,
			),
			fwd_from : $client->messageFwdHeader(
				imported : true,
				saved_out : true,
				from_id : $client->peerUser(...),
				from_name : 'bfAHT6o4q7vh8yGm',
				date : 51,
				channel_post : 18,
				post_author : '0dLCfJG4NQ3jpI5g',
				saved_from_peer : $client->peerUser(...),
				saved_from_msg_id : 5,
				saved_from_id : $client->peerUser(...),
				saved_from_name : '0TbuNeQ38rHfvayS',
				saved_date : 33,
				psa_type : 'mebwyR3Jpjf70QAa',
			),
			via_bot_id : -8289535009606932500,
			via_business_bot_id : 6723982353205976733,
			reply_to : $client->messageReplyHeader(
				reply_to_scheduled : true,
				forum_topic : true,
				quote : true,
				reply_to_msg_id : 39,
				reply_to_peer_id : $client->peerUser(...),
				reply_from : $client->messageFwdHeader(...),
				reply_media : $client->messageMediaEmpty(...),
				reply_to_top_id : 93,
				quote_text : '1KhC5vmbIectJXur',
				quote_entities : array(
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
				quote_offset : 27,
				todo_item_id : 26,
			),
			date : 50,
			message : 'MryoYGXh4NL87ubV',
			media : $client->messageMediaEmpty(),
			reply_markup : $client->replyKeyboardHide(
				selective : true,
			),
			entities : array(
				$client->messageEntityUnknown(
					offset : 85,
					length : 37,
				),
				$client->messageEntityMention(
					offset : 90,
					length : 18,
				),
				$client->messageEntityHashtag(
					offset : 49,
					length : 11,
				),
				$client->messageEntityBotCommand(
					offset : 74,
					length : 86,
				),
				$client->messageEntityUrl(
					offset : 72,
					length : 75,
				),
				$client->messageEntityEmail(
					offset : 66,
					length : 81,
				),
				$client->messageEntityBold(
					offset : 54,
					length : 18,
				),
				$client->messageEntityItalic(
					offset : 29,
					length : 81,
				),
				$client->messageEntityCode(
					offset : 62,
					length : 80,
				),
				$client->messageEntityPre(
					offset : 83,
					length : 44,
					language : 'hGPxZavbFqg9EwmT',
				),
				$client->messageEntityTextUrl(
					offset : 1,
					length : 12,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 28,
					length : 65,
					user_id : -3545425566827720952,
				),
				$client->inputMessageEntityMentionName(
					offset : 72,
					length : 5,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 81,
					length : 26,
				),
				$client->messageEntityCashtag(
					offset : 1,
					length : 30,
				),
				$client->messageEntityUnderline(
					offset : 9,
					length : 81,
				),
				$client->messageEntityStrike(
					offset : 80,
					length : 57,
				),
				$client->messageEntityBankCard(
					offset : 94,
					length : 68,
				),
				$client->messageEntitySpoiler(
					offset : 34,
					length : 21,
				),
				$client->messageEntityCustomEmoji(
					offset : 72,
					length : 96,
					document_id : 8107847478280647226,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 73,
					length : 75,
				),
			),
			views : 57,
			forwards : 39,
			replies : $client->messageReplies(
				comments : true,
				replies : 50,
				replies_pts : 31,
				recent_repliers : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				channel_id : -7744158715832708387,
				max_id : 2,
				read_max_id : 3,
			),
			edit_date : 57,
			post_author : 'cIA5PsX6FTEYBNzy',
			grouped_id : -1006152647001585733,
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
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'uAh1VTSj8t6rmR0i',
					reason : 'SVO6pZUPYEFXoI1Q',
					text : 'YfMbagxhR6OUyoNW',
				),
			),
			ttl_period : 81,
			quick_reply_shortcut_id : 97,
			effect : -8541865449982232330,
			factcheck : $client->factCheck(
				need_check : true,
				country : 'xTU64ba9FwSCmgs5',
				text : $client->textWithEntities(...),
				hash : 4973516017672318278,
			),
			report_delivery_until_date : 59,
			paid_message_stars : 2987647545987513047,
			suggested_post : $client->suggestedPost(
				accepted : true,
				rejected : true,
				price : $client->starsAmount(...),
				schedule_date : 78,
			),
		),
		$client->messageService(
			out : true,
			mentioned : true,
			media_unread : true,
			reactions_are_possible : true,
			silent : true,
			post : true,
			legacy : true,
			id : 54,
			from_id : $client->peerUser(
				user_id : -2784034410300048010,
			),
			peer_id : $client->peerUser(
				user_id : 4040590094238964156,
			),
			saved_peer_id : $client->peerUser(
				user_id : 2708372953723874213,
			),
			reply_to : $client->messageReplyHeader(
				reply_to_scheduled : true,
				forum_topic : true,
				quote : true,
				reply_to_msg_id : 30,
				reply_to_peer_id : $client->peerUser(...),
				reply_from : $client->messageFwdHeader(...),
				reply_media : $client->messageMediaEmpty(...),
				reply_to_top_id : 64,
				quote_text : '85ObtwnNQayDprsu',
				quote_entities : array(
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
				quote_offset : 4,
				todo_item_id : 53,
			),
			date : 84,
			action : $client->messageActionEmpty(),
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
			ttl_period : 90,
		),
	),
	new_encrypted_messages : array(
		$client->encryptedMessage(
			random_id : -6820582775530891254,
			chat_id : 64,
			date : 31,
			bytes : 'D8a?LiveProtoA??J"',
			file : $client->encryptedFileEmpty(),
		),
		$client->encryptedMessageService(
			random_id : 1576633337257795446,
			chat_id : 80,
			date : 86,
			bytes : '????LiveProtoz?',
		),
	),
	other_updates : array(
		$client->updateNewMessage(
			message : $client->messageEmpty(
				id : 75,
				peer_id : $client->peerUser(...),
			),
			pts : 1,
			pts_count : 62,
		),
		$client->updateMessageID(
			id : 68,
			random_id : -5987826719823007532,
		),
		$client->updateDeleteMessages(
			messages : array(96),
			pts : 53,
			pts_count : 48,
		),
		$client->updateUserTyping(
			user_id : -7804017460207023,
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatUserTyping(
			chat_id : -7308834608621835312,
			from_id : $client->peerUser(
				user_id : 8513217654181210805,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatParticipants(
			participants : $client->chatParticipantsForbidden(
				chat_id : 4835395081704253194,
				self_participant : $client->chatParticipant(...),
			),
		),
		$client->updateUserStatus(
			user_id : 6563005984832712272,
			status : $client->userStatusEmpty(),
		),
		$client->updateUserName(
			user_id : 372184781945166857,
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
			hash : 4656835557844964325,
			date : 93,
			device : 'gDz6WMuo2aOqvjpw',
			location : 'gzeBiUsRny5vDo2Y',
		),
		$client->updateNewEncryptedMessage(
			message : $client->encryptedMessage(
				random_id : -4029425788416644219,
				chat_id : 10,
				date : 13,
				bytes : 'N???LiveProtoԏ*?',
				file : $client->encryptedFileEmpty(...),
			),
			qts : 39,
		),
		$client->updateEncryptedChatTyping(
			chat_id : 62,
		),
		$client->updateEncryption(
			chat : $client->encryptedChatEmpty(
				id : 27,
			),
			date : 28,
		),
		$client->updateEncryptedMessagesRead(
			chat_id : 72,
			max_date : 42,
			date : 8,
		),
		$client->updateChatParticipantAdd(
			chat_id : -6544956365897676380,
			user_id : -3350062714878995362,
			inviter_id : 8544306170642001256,
			date : 10,
			version : 58,
		),
		$client->updateChatParticipantDelete(
			chat_id : -1076346949776759736,
			user_id : -8961749094882211225,
			version : 88,
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
					id : 85,
					ip_address : '127.0.0.1',
					port : 89,
					secret : '?a	acLiveProto???9',
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
				mute_until : 22,
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
			inbox_date : 100,
			type : 'eikvwxIRBAoKDf23',
			message : '4DNYeP5gS6rCBLvq',
			media : $client->messageMediaEmpty(),
			entities : array(
				$client->messageEntityUnknown(
					offset : 2,
					length : 74,
				),
				$client->messageEntityMention(
					offset : 37,
					length : 16,
				),
				$client->messageEntityHashtag(
					offset : 51,
					length : 22,
				),
				$client->messageEntityBotCommand(
					offset : 3,
					length : 61,
				),
				$client->messageEntityUrl(
					offset : 17,
					length : 98,
				),
				$client->messageEntityEmail(
					offset : 14,
					length : 66,
				),
				$client->messageEntityBold(
					offset : 38,
					length : 55,
				),
				$client->messageEntityItalic(
					offset : 92,
					length : 94,
				),
				$client->messageEntityCode(
					offset : 4,
					length : 67,
				),
				$client->messageEntityPre(
					offset : 88,
					length : 60,
					language : '6X2hR4zABSuDFxw3',
				),
				$client->messageEntityTextUrl(
					offset : 0,
					length : 59,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 64,
					length : 92,
					user_id : -3120249012283183385,
				),
				$client->inputMessageEntityMentionName(
					offset : 50,
					length : 99,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 84,
					length : 18,
				),
				$client->messageEntityCashtag(
					offset : 86,
					length : 59,
				),
				$client->messageEntityUnderline(
					offset : 21,
					length : 42,
				),
				$client->messageEntityStrike(
					offset : 42,
					length : 59,
				),
				$client->messageEntityBankCard(
					offset : 98,
					length : 90,
				),
				$client->messageEntitySpoiler(
					offset : 83,
					length : 53,
				),
				$client->messageEntityCustomEmoji(
					offset : 29,
					length : 10,
					document_id : 1723466018238628609,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 83,
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
					users : array(-1322131333717462784),
				),
				$client->privacyValueDisallowContacts(),
				$client->privacyValueDisallowAll(),
				$client->privacyValueDisallowUsers(
					users : array(-216964686262400474),
				),
				$client->privacyValueAllowChatParticipants(
					chats : array(1387445953736024678),
				),
				$client->privacyValueDisallowChatParticipants(
					chats : array(-2287916494917896688),
				),
				$client->privacyValueAllowCloseFriends(),
				$client->privacyValueAllowPremium(),
				$client->privacyValueAllowBots(),
				$client->privacyValueDisallowBots(),
			),
		),
		$client->updateUserPhone(
			user_id : -129754814239947432,
			phone : '+1234567890',
		),
		$client->updateReadHistoryInbox(
			folder_id : 48,
			peer : $client->peerUser(
				user_id : 1343887209418090524,
			),
			max_id : 5,
			still_unread_count : 54,
			pts : 65,
			pts_count : 65,
		),
		$client->updateReadHistoryOutbox(
			peer : $client->peerUser(
				user_id : -9024002842038884808,
			),
			max_id : 41,
			pts : 97,
			pts_count : 45,
		),
		$client->updateWebPage(
			webpage : $client->webPageEmpty(
				id : -4852557019662691197,
				url : 'https://docs.liveproto.dev',
			),
			pts : 24,
			pts_count : 18,
		),
		$client->updateReadMessagesContents(
			messages : array(60),
			pts : 63,
			pts_count : 46,
			date : 90,
		),
		$client->updateChannelTooLong(
			channel_id : 5204858125833769388,
			pts : 11,
		),
		$client->updateChannel(
			channel_id : 1908113896182470311,
		),
		$client->updateNewChannelMessage(
			message : $client->messageEmpty(
				id : 47,
				peer_id : $client->peerUser(...),
			),
			pts : 71,
			pts_count : 88,
		),
		$client->updateReadChannelInbox(
			folder_id : 41,
			channel_id : -8749668022211758042,
			max_id : 35,
			still_unread_count : 8,
			pts : 90,
		),
		$client->updateDeleteChannelMessages(
			channel_id : 3287744026499100626,
			messages : array(36),
			pts : 5,
			pts_count : 79,
		),
		$client->updateChannelMessageViews(
			channel_id : -4778876606392929148,
			id : 85,
			views : 54,
		),
		$client->updateChatParticipantAdmin(
			chat_id : 6942157171891223567,
			user_id : 2128400594463374411,
			is_admin : $client->boolFalse(),
			version : 32,
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
			order : array(-5510045998102551177),
		),
		$client->updateStickerSets(
			masks : true,
			emojis : true,
		),
		$client->updateSavedGifs(),
		$client->updateBotInlineQuery(
			query_id : -495109533084024665,
			user_id : 2654032197071785557,
			query : '061sdWae5oYqzDc3',
			geo : $client->geoPointEmpty(),
			peer_type : $client->inlineQueryPeerTypeSameBotPM(),
			offset : 'vfzC9hYlNbXqWweu',
		),
		$client->updateBotInlineSend(
			user_id : 994947845595706788,
			query : 'DFkWnTAiPmwg56xl',
			geo : $client->geoPointEmpty(),
			id : 'zYDku7MfVPrCI8ZU',
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 17,
				id : -1839501796478985700,
				access_hash : 5810379178806971219,
			),
		),
		$client->updateEditChannelMessage(
			message : $client->messageEmpty(
				id : 83,
				peer_id : $client->peerUser(...),
			),
			pts : 21,
			pts_count : 45,
		),
		$client->updateBotCallbackQuery(
			query_id : 3639456627280490696,
			user_id : 1360565356446217819,
			peer : $client->peerUser(
				user_id : -8968048004523613832,
			),
			msg_id : 7,
			chat_instance : -7014977938130058899,
			data : '??4?LiveProto?{/',
			game_short_name : 'gm9Fn7cBjKdGS1P8',
		),
		$client->updateEditMessage(
			message : $client->messageEmpty(
				id : 29,
				peer_id : $client->peerUser(...),
			),
			pts : 79,
			pts_count : 47,
		),
		$client->updateInlineBotCallbackQuery(
			query_id : -8964448039559574515,
			user_id : 7516281086521234822,
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 78,
				id : -8259914374237719027,
				access_hash : 7213229789256425431,
			),
			chat_instance : 2281002523129373211,
			data : '?N?k;LiveProtoԏ??',
			game_short_name : 'mcUXeydv28JGNbxW',
		),
		$client->updateReadChannelOutbox(
			channel_id : -3906660521336317918,
			max_id : 4,
		),
		$client->updateDraftMessage(
			peer : $client->peerUser(
				user_id : -8955921760889404639,
			),
			top_msg_id : 80,
			saved_peer_id : $client->peerUser(
				user_id : 3098606018324279548,
			),
			draft : $client->draftMessageEmpty(
				date : 43,
			),
		),
		$client->updateReadFeaturedStickers(),
		$client->updateRecentStickers(),
		$client->updateConfig(),
		$client->updatePtsChanged(),
		$client->updateChannelWebPage(
			channel_id : 8185653407939935836,
			webpage : $client->webPageEmpty(
				id : -2007436707593245776,
				url : 'https://docs.liveproto.dev',
			),
			pts : 44,
			pts_count : 68,
		),
		$client->updateDialogPinned(
			pinned : true,
			folder_id : 58,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
		),
		$client->updatePinnedDialogs(
			folder_id : 34,
			order : array(
				$client->dialogPeer(
					peer : $client->peerUser(...),
				),
				$client->dialogPeerFolder(
					folder_id : 0,
				),
			),
		),
		$client->updateBotWebhookJSON(
			data : $client->dataJSON(
				data : 'DdyfukmwQgblcr8h',
			),
		),
		$client->updateBotWebhookJSONQuery(
			query_id : 6646410289981726319,
			data : $client->dataJSON(
				data : 'HE7Uj9GfdnmKVb8I',
			),
			timeout : 1,
		),
		$client->updateBotShippingQuery(
			query_id : -6418601204325657968,
			user_id : -2729450076675610941,
			payload : '??_?LiveProto?`|?',
			shipping_address : $client->postAddress(
				street_line1 : '3pJSoajfZLiYdebD',
				street_line2 : 'K8JGHZ7MuLwlmazS',
				city : 'imWjDKQGbcBvCMYk',
				state : 'jzWnUdeQOApPlcLX',
				country_iso2 : 'pDAC1cZkWvMwRbso',
				post_code : 'CyAoZ6RTuVpeklE4',
			),
		),
		$client->updateBotPrecheckoutQuery(
			query_id : 1371908394064971310,
			user_id : -5266046478625524160,
			payload : '?{Gu?LiveProtoA?? ',
			info : $client->paymentRequestedInfo(
				name : 'kBWRzrxyInEULgqZ',
				phone : '+1234567890',
				email : 'reply@liveproto.dev',
				shipping_address : $client->postAddress(...),
			),
			shipping_option_id : 'owa5SDRFMisOu70f',
			currency : 'x2ep5E8JgTZitYCa',
			total_amount : -1926354298215759844,
		),
		$client->updatePhoneCall(
			phone_call : $client->phoneCallEmpty(
				id : -8107739672269442861,
			),
		),
		$client->updateLangPackTooLong(
			lang_code : 'XpDxIGvB4RY8yOW6',
		),
		$client->updateLangPack(
			difference : $client->langPackDifference(
				lang_code : 'r8DOo1Sw9U2zvnmY',
				from_version : 76,
				version : 51,
				strings : array(
					$client->langPackString(...),
					$client->langPackStringPluralized(...),
					$client->langPackStringDeleted(...),
				),
			),
		),
		$client->updateFavedStickers(),
		$client->updateChannelReadMessagesContents(
			channel_id : -4931066437227827864,
			top_msg_id : 69,
			saved_peer_id : $client->peerUser(
				user_id : -4204937360236551873,
			),
			messages : array(20),
		),
		$client->updateContactsReset(),
		$client->updateChannelAvailableMessages(
			channel_id : -7994952707973162173,
			available_min_id : 13,
		),
		$client->updateDialogUnreadMark(
			unread : true,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
			saved_peer_id : $client->peerUser(
				user_id : 1818162847589125850,
			),
		),
		$client->updateMessagePoll(
			poll_id : 5329693085858172016,
			poll : $client->poll(
				id : 8801513293660401871,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 49,
				close_date : 5,
			),
			results : $client->pollResults(
				min : true,
				results : array(
					$client->pollAnswerVoters(...),
				),
				total_voters : 24,
				recent_voters : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				solution : '7QbheD8FNCVPf3zA',
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
				user_id : 1277792266177974415,
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
				until_date : 83,
			),
			version : 87,
		),
		$client->updateFolderPeers(
			folder_peers : array(
				$client->folderPeer(
					peer : $client->peerUser(...),
					folder_id : 61,
				),
			),
			pts : 82,
			pts_count : 69,
		),
		$client->updatePeerSettings(
			peer : $client->peerUser(
				user_id : 2627420368685309057,
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
				geo_distance : 33,
				request_chat_title : 'pJZ4Qin0GCBoq3KD',
				request_chat_date : 32,
				business_bot_id : 6570445317435415935,
				business_bot_manage_url : 'https://docs.liveproto.dev',
				charge_paid_message_stars : 4686250764896551312,
				registration_month : 'GdTpOKWEiD5v8yNY',
				phone_country : '+1234567890',
				name_change_date : 93,
				photo_change_date : 19,
			),
		),
		$client->updatePeerLocated(
			peers : array(
				$client->peerLocated(
					peer : $client->peerUser(...),
					expires : 62,
					distance : 41,
				),
				$client->peerSelfLocated(
					expires : 65,
				),
			),
		),
		$client->updateNewScheduledMessage(
			message : $client->messageEmpty(
				id : 93,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteScheduledMessages(
			peer : $client->peerUser(
				user_id : -6309609251453606470,
			),
			messages : array(83),
			sent_messages : array(53),
		),
		$client->updateTheme(
			theme : $client->theme(
				creator : true,
				default : true,
				for_chat : true,
				id : -9077472918050965053,
				access_hash : 1757885655540134740,
				slug : 'FfiSsBnIzqGZkEKw',
				title : 'dNE5ufRwc8zhPDQ3',
				document : $client->documentEmpty(...),
				settings : array(
					$client->themeSettings(...),
				),
				emoticon : 'SI4agRWVElZzJTLo',
				installs_count : 59,
			),
		),
		$client->updateGeoLiveViewed(
			peer : $client->peerUser(
				user_id : 6146893394811604587,
			),
			msg_id : 54,
		),
		$client->updateLoginToken(),
		$client->updateMessagePollVote(
			poll_id : 2036825603876894620,
			peer : $client->peerUser(
				user_id : 23675723386394372,
			),
			options : array('d?<?LiveProto?:i'),
			qts : 52,
		),
		$client->updateDialogFilter(
			id : 85,
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
				id : 97,
				title : $client->textWithEntities(...),
				emoticon : 'G1T5aDchqz8ZlUwW',
				color : 92,
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
			order : array(10),
		),
		$client->updateDialogFilters(),
		$client->updatePhoneCallSignalingData(
			phone_call_id : -8107552903802034065,
			data : '?p??GLiveProto?j?W?',
		),
		$client->updateChannelMessageForwards(
			channel_id : -7289058048296634767,
			id : 74,
			forwards : 63,
		),
		$client->updateReadChannelDiscussionInbox(
			channel_id : 4600149273867750289,
			top_msg_id : 6,
			read_max_id : 83,
			broadcast_id : -1104017801778930771,
			broadcast_post : 99,
		),
		$client->updateReadChannelDiscussionOutbox(
			channel_id : -4048846304020166589,
			top_msg_id : 22,
			read_max_id : 39,
		),
		$client->updatePeerBlocked(
			blocked : true,
			blocked_my_stories_from : true,
			peer_id : $client->peerUser(
				user_id : -6758684754958909744,
			),
		),
		$client->updateChannelUserTyping(
			channel_id : -2704873588019884405,
			top_msg_id : 43,
			from_id : $client->peerUser(
				user_id : 3705817102227786380,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updatePinnedMessages(
			pinned : true,
			peer : $client->peerUser(
				user_id : -2456884698477875658,
			),
			messages : array(73),
			pts : 69,
			pts_count : 88,
		),
		$client->updatePinnedChannelMessages(
			pinned : true,
			channel_id : -3516853799599061310,
			messages : array(86),
			pts : 16,
			pts_count : 65,
		),
		$client->updateChat(
			chat_id : -8662257215266832995,
		),
		$client->updateGroupCallParticipants(
			call : $client->inputGroupCall(
				id : 2691569535653403787,
				access_hash : -693240030631802947,
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
					date : 83,
					active_date : 31,
					source : 9,
					volume : 23,
					about : '4YorWB7wKNDzTdFe',
					raise_hand_rating : -7253346737057423285,
					video : $client->groupCallParticipantVideo(...),
					presentation : $client->groupCallParticipantVideo(...),
				),
			),
			version : 34,
		),
		$client->updateGroupCall(
			chat_id : -5301308034539763172,
			call : $client->groupCallDiscarded(
				id : -4834235648224760647,
				access_hash : 6964730284699405610,
				duration : 29,
			),
		),
		$client->updatePeerHistoryTTL(
			peer : $client->peerUser(
				user_id : -3245547152420678553,
			),
			ttl_period : 51,
		),
		$client->updateChatParticipant(
			chat_id : -2146138415927582587,
			date : 22,
			actor_id : 3799656456619111774,
			user_id : -6758665955285727408,
			prev_participant : $client->chatParticipant(
				user_id : -8941181394881008751,
				inviter_id : -4595989657544195094,
				date : 34,
			),
			new_participant : $client->chatParticipant(
				user_id : 6896103063343894570,
				inviter_id : -5607971511623567451,
				date : 80,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'Sh1nL2u9vw7FCY5W',
				admin_id : -3398365462056697319,
				date : 99,
				start_date : 100,
				expire_date : 97,
				usage_limit : 47,
				usage : 84,
				requested : 18,
				subscription_expired : 21,
				title : 'aF2h3jdTiv7XuL4p',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 2,
		),
		$client->updateChannelParticipant(
			via_chatlist : true,
			channel_id : -8684974576389163472,
			date : 21,
			actor_id : 2983346845871259794,
			user_id : -6465395867572547835,
			prev_participant : $client->channelParticipant(
				user_id : 2515961370720256633,
				date : 68,
				subscription_until_date : 87,
			),
			new_participant : $client->channelParticipant(
				user_id : 8216727027477601701,
				date : 87,
				subscription_until_date : 20,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'OjHp6PmU5hlokMW7',
				admin_id : 610985887956180278,
				date : 42,
				start_date : 40,
				expire_date : 7,
				usage_limit : 90,
				usage : 47,
				requested : 5,
				subscription_expired : 76,
				title : 'IjUVbQXhFAuqa0CH',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 64,
		),
		$client->updateBotStopped(
			user_id : -5983217808777589421,
			date : 45,
			stopped : $client->boolFalse(),
			qts : 10,
		),
		$client->updateGroupCallConnection(
			presentation : true,
			params : $client->dataJSON(
				data : 'qmji7B1bOdKEL2Pw',
			),
		),
		$client->updateBotCommands(
			peer : $client->peerUser(
				user_id : -2105598131748316517,
			),
			bot_id : -5565134205474354957,
			commands : array(
				$client->botCommand(
					command : 'gkmzjSsfo3pJK8lu',
					description : 'PvI0H8m5N4exLsJg',
				),
			),
		),
		$client->updatePendingJoinRequests(
			peer : $client->peerUser(
				user_id : 7907469446154302451,
			),
			requests_pending : 46,
			recent_requesters : array(2917908835807183964),
		),
		$client->updateBotChatInviteRequester(
			peer : $client->peerUser(
				user_id : 4257046606667635580,
			),
			date : 94,
			user_id : -3226762397530967131,
			about : 'doaBhs46bQrvpeZU',
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'aogc48IH0AqunMw3',
				admin_id : 5100468909402092666,
				date : 37,
				start_date : 32,
				expire_date : 79,
				usage_limit : 20,
				usage : 59,
				requested : 97,
				subscription_expired : 79,
				title : 'Wd48NMmvjHpI9Kfe',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 38,
		),
		$client->updateMessageReactions(
			peer : $client->peerUser(
				user_id : -3261288002021167112,
			),
			msg_id : 62,
			top_msg_id : 21,
			saved_peer_id : $client->peerUser(
				user_id : 1942496484280285762,
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
			query_id : -8997479551197622113,
		),
		$client->updateBotMenuButton(
			bot_id : 2347979462699112971,
			button : $client->botMenuButtonDefault(),
		),
		$client->updateSavedRingtones(),
		$client->updateTranscribedAudio(
			pending : true,
			peer : $client->peerUser(
				user_id : -4247520179225565113,
			),
			msg_id : 63,
			transcription_id : 2576387718224807203,
			text : 'UR3jyk2Ec1o8SBeD',
		),
		$client->updateReadFeaturedEmojiStickers(),
		$client->updateUserEmojiStatus(
			user_id : -7137696373057202623,
			emoji_status : $client->emojiStatusEmpty(),
		),
		$client->updateRecentEmojiStatuses(),
		$client->updateRecentReactions(),
		$client->updateMoveStickerSetToTop(
			masks : true,
			emojis : true,
			stickerset : -8919092451232802465,
		),
		$client->updateMessageExtendedMedia(
			peer : $client->peerUser(
				user_id : -5392160197427603004,
			),
			msg_id : 6,
			extended_media : array(
				$client->messageExtendedMediaPreview(
					w : 87,
					h : 94,
					thumb : $client->photoSizeEmpty(...),
					video_duration : 83,
				),
				$client->messageExtendedMedia(
					media : $client->messageMediaEmpty(...),
				),
			),
		),
		$client->updateChannelPinnedTopic(
			pinned : true,
			channel_id : -1649229268666748187,
			topic_id : 52,
		),
		$client->updateChannelPinnedTopics(
			channel_id : -4711567642336651467,
			order : array(40),
		),
		$client->updateUser(
			user_id : 242264224201716057,
		),
		$client->updateAutoSaveSettings(),
		$client->updateStory(
			peer : $client->peerUser(
				user_id : 5368174679127978217,
			),
			story : $client->storyItemDeleted(
				id : 36,
			),
		),
		$client->updateReadStories(
			peer : $client->peerUser(
				user_id : 3731240462838574287,
			),
			max_id : 74,
		),
		$client->updateStoryID(
			id : 28,
			random_id : -261989945214757076,
		),
		$client->updateStoriesStealthMode(
			stealth_mode : $client->storiesStealthMode(
				active_until_date : 45,
				cooldown_until_date : 90,
			),
		),
		$client->updateSentStoryReaction(
			peer : $client->peerUser(
				user_id : -908934760917737725,
			),
			story_id : 96,
			reaction : $client->reactionEmpty(),
		),
		$client->updateBotChatBoost(
			peer : $client->peerUser(
				user_id : 7853610989355951506,
			),
			boost : $client->boost(
				gift : true,
				giveaway : true,
				unclaimed : true,
				id : 'DP2jxoOTECH6tZFQ',
				user_id : -638417202812227372,
				giveaway_msg_id : 12,
				date : 62,
				expires : 9,
				used_gift_slug : '3gSfq1FevRkdyIUx',
				multiplier : 6,
				stars : -378097891320959468,
			),
			qts : 24,
		),
		$client->updateChannelViewForumAsMessages(
			channel_id : -1416968152647150480,
			enabled : $client->boolFalse(),
		),
		$client->updatePeerWallpaper(
			wallpaper_overridden : true,
			peer : $client->peerUser(
				user_id : -6418306408821556876,
			),
			wallpaper : $client->wallPaper(
				id : 9060175582203759970,
				creator : true,
				default : true,
				pattern : true,
				dark : true,
				access_hash : 7409106778506481691,
				slug : 'TEUfR2LYmKHb3qIJ',
				document : $client->documentEmpty(...),
				settings : $client->wallPaperSettings(...),
			),
		),
		$client->updateBotMessageReaction(
			peer : $client->peerUser(
				user_id : -5344299474948778009,
			),
			msg_id : 90,
			date : 39,
			actor : $client->peerUser(
				user_id : 9176147822764001464,
			),
			old_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'CHGvY2NaJxKj6bWF',
				),
				$client->reactionCustomEmoji(
					document_id : 2545562120075529550,
				),
				$client->reactionPaid(),
			),
			new_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'oyTHX45b91akCQwh',
				),
				$client->reactionCustomEmoji(
					document_id : 6962340192804062157,
				),
				$client->reactionPaid(),
			),
			qts : 58,
		),
		$client->updateBotMessageReactions(
			peer : $client->peerUser(
				user_id : -828587779202294300,
			),
			msg_id : 52,
			date : 43,
			reactions : array(
				$client->reactionCount(
					chosen_order : 73,
					reaction : $client->reactionEmpty(...),
					count : 94,
				),
			),
			qts : 19,
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
					folder_id : 76,
				),
			),
		),
		$client->updateSavedReactionTags(),
		$client->updateSmsJob(
			job_id : 'g2sEACwqJpBbmHvl',
		),
		$client->updateQuickReplies(
			quick_replies : array(
				$client->quickReply(
					shortcut_id : 6,
					shortcut : 'fzRe0u8jlr2cqpU5',
					top_message : 29,
					count : 27,
				),
			),
		),
		$client->updateNewQuickReply(
			quick_reply : $client->quickReply(
				shortcut_id : 32,
				shortcut : '5Cp8s9ByNfZRPiU2',
				top_message : 4,
				count : 21,
			),
		),
		$client->updateDeleteQuickReply(
			shortcut_id : 85,
		),
		$client->updateQuickReplyMessage(
			message : $client->messageEmpty(
				id : 27,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteQuickReplyMessages(
			shortcut_id : 26,
			messages : array(11),
		),
		$client->updateBotBusinessConnect(
			connection : $client->botBusinessConnection(
				disabled : true,
				connection_id : 'fF7leMLpCWIPUS2A',
				user_id : -217877365834810440,
				dc_id : 44,
				date : 23,
				rights : $client->businessBotRights(...),
			),
			qts : 51,
		),
		$client->updateBotNewBusinessMessage(
			connection_id : 'MTzoe6NxEgGk0IBH',
			message : $client->messageEmpty(
				id : 66,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 99,
				peer_id : $client->peerUser(...),
			),
			qts : 64,
		),
		$client->updateBotEditBusinessMessage(
			connection_id : 'gAiokevcR02BqbHu',
			message : $client->messageEmpty(
				id : 100,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 76,
				peer_id : $client->peerUser(...),
			),
			qts : 94,
		),
		$client->updateBotDeleteBusinessMessage(
			connection_id : '3thEvGyOmTkPbKrn',
			peer : $client->peerUser(
				user_id : -8395374118884306825,
			),
			messages : array(83),
			qts : 98,
		),
		$client->updateNewStoryReaction(
			story_id : 73,
			peer : $client->peerUser(
				user_id : -5615455963946060583,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->updateStarsBalance(
			balance : $client->starsAmount(
				amount : -5761305981342870049,
				nanos : 16,
			),
		),
		$client->updateBusinessBotCallbackQuery(
			query_id : -4686461524481773988,
			user_id : -1709341071431016119,
			connection_id : 'WsizFd3n5L9KEHgI',
			message : $client->messageEmpty(
				id : 91,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 74,
				peer_id : $client->peerUser(...),
			),
			chat_instance : -8673394592009633469,
			data : '?????LiveProtoT?Z?1',
		),
		$client->updateStarsRevenueStatus(
			peer : $client->peerUser(
				user_id : -5885044470427429735,
			),
			status : $client->starsRevenueStatus(
				withdrawal_enabled : true,
				current_balance : $client->starsAmount(...),
				available_balance : $client->starsAmount(...),
				overall_revenue : $client->starsAmount(...),
				next_withdrawal_at : 55,
			),
		),
		$client->updateBotPurchasedPaidMedia(
			user_id : 6139303125764821919,
			payload : 'BFXEd4PJRwkbHV67',
			qts : 83,
		),
		$client->updatePaidReactionPrivacy(
			private : $client->paidReactionPrivacyDefault(),
		),
		$client->updateSentPhoneCode(
			sent_code : $client->auth->sentCode(
				type : $client->auth->sentCodeTypeApp(...),
				phone_code_hash : '+1234567890',
				next_type : $client->auth->codeTypeSms(...),
				timeout : 41,
			),
		),
		$client->updateGroupCallChainBlocks(
			call : $client->inputGroupCall(
				id : 2327883294654657294,
				access_hash : -2287458292635540172,
			),
			sub_chain_id : 88,
			blocks : array(' 8o2?LiveProto`?,?'),
			next_offset : 68,
		),
		$client->updateReadMonoForumInbox(
			channel_id : -4233657815592602463,
			saved_peer_id : $client->peerUser(
				user_id : 5023719832452450197,
			),
			read_max_id : 6,
		),
		$client->updateReadMonoForumOutbox(
			channel_id : 3225870854414017494,
			saved_peer_id : $client->peerUser(
				user_id : -7913725785750989740,
			),
			read_max_id : 95,
		),
		$client->updateMonoForumNoPaidException(
			exception : true,
			channel_id : 929859442016217465,
			saved_peer_id : $client->peerUser(
				user_id : -4021503965054936262,
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -5868933140401781203,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -6890973691361344381,
			title : 'pPRYaDdMco1nWX23',
			photo : $client->chatPhotoEmpty(),
			participants_count : 23,
			date : 12,
			version : 2,
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
				until_date : 18,
			),
		),
		$client->chatForbidden(
			id : -6201120964522352891,
			title : 'gIEx8StidncQweGJ',
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
			id : 2933438670875575581,
			access_hash : -954890253381913943,
			title : 'NeLh1UB472bWSpwj',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 77,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'xXiRvWhZGTjz0rsY',
					reason : 'LtBwr5EG0NdFzeHu',
					text : '6zoVOABin93CSaxT',
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
				until_date : 84,
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
				until_date : 20,
			),
			participants_count : 67,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 81,
			color : $client->peerColor(
				color : 52,
				background_emoji_id : -7868517961765748557,
			),
			profile_color : $client->peerColor(
				color : 86,
				background_emoji_id : 1953311724060506745,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 79,
			subscription_until_date : 33,
			bot_verification_icon : -3329219349467520456,
			send_paid_messages_stars : -2599367705615656992,
			linked_monoforum_id : 1643970222008999605,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 337117996831962006,
			access_hash : 8020185520351731731,
			title : 'gOjv6V5FnCcfidNe',
			until_date : 4,
		),
	),
	users : array(
		$client->userEmpty(
			id : -1094482867476198634,
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
			id : 8350601974188356155,
			access_hash : 8400316456523889478,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 57,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'l0W5vzNVHIf8wyO7',
					reason : 'aSmo1QyHTdgWtGvX',
					text : 'VBS04Uj1pyrhTzvW',
				),
			),
			bot_inline_placeholder : 'LybJnr7R6oVXlB4h',
			lang_code : 'O2ncwLTUiPd4Nst1',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 53,
			color : $client->peerColor(
				color : 86,
				background_emoji_id : -8958376809020205989,
			),
			profile_color : $client->peerColor(
				color : 6,
				background_emoji_id : -2986978129005317881,
			),
			bot_active_users : 39,
			bot_verification_icon : -3263616404164176395,
			send_paid_messages_stars : 4488602513467585163,
		),
	),
	state : $client->updates->state(
		pts : 66,
		qts : 79,
		date : 86,
		seq : 44,
		unread_count : 35,
	),
);
```