# updates.differenceSlice

**Description** : *Incomplete list of occurred events*

**Layer** : 211

```tl
updates.differenceSlice#a8fb1981 new_messages:Vector<Message> new_encrypted_messages:Vector<EncryptedMessage> other_updates:Vector<Update> chats:Vector<Chat> users:Vector<User> intermediate_state:updates.State = updates.Difference;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>new_messages</mark> | [`Vector<Message>`](type/Message) | List of new messages |
| <mark>new_encrypted_messages</mark> | [`Vector<EncryptedMessage>`](type/EncryptedMessage) | New messages from the encrypted event sequence |
| <mark>other_updates</mark> | [`Vector<Update>`](type/Update) | List of updates |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | List of chats mentioned in events |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of users mentioned in events |
| <mark>intermediate_state</mark> | [`updates.State`](type/updates.State) | Intermediary state |

---

## Type

[updates.Difference](type/updates.Difference)

---

## Example

```php
$updatesDifference = $client->updates->differenceSlice(
	new_messages : array(
		$client->messageEmpty(
			id : 90,
			peer_id : $client->peerUser(
				user_id : -8607878158352073047,
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
			id : 42,
			from_id : $client->peerUser(
				user_id : 7832224490417185690,
			),
			from_boosts_applied : 60,
			peer_id : $client->peerUser(
				user_id : 6066441525575611324,
			),
			saved_peer_id : $client->peerUser(
				user_id : -4254770944613413661,
			),
			fwd_from : $client->messageFwdHeader(
				imported : true,
				saved_out : true,
				from_id : $client->peerUser(...),
				from_name : 'y4oAxRiUGXphmHzY',
				date : 11,
				channel_post : 24,
				post_author : 'ur1yg3lULRzoGwpP',
				saved_from_peer : $client->peerUser(...),
				saved_from_msg_id : 1,
				saved_from_id : $client->peerUser(...),
				saved_from_name : 'rm8hd7SRAOjKEiCo',
				saved_date : 30,
				psa_type : 'Z6BMHjqAN2PyFODU',
			),
			via_bot_id : -4172822338183099293,
			via_business_bot_id : 4482593041982287652,
			reply_to : $client->messageReplyHeader(
				reply_to_scheduled : true,
				forum_topic : true,
				quote : true,
				reply_to_msg_id : 30,
				reply_to_peer_id : $client->peerUser(...),
				reply_from : $client->messageFwdHeader(...),
				reply_media : $client->messageMediaEmpty(...),
				reply_to_top_id : 63,
				quote_text : 'QXPm42U3ofSRMdub',
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
				quote_offset : 25,
				todo_item_id : 0,
			),
			date : 38,
			message : 'F57y6NQzBVWOks1K',
			media : $client->messageMediaEmpty(),
			reply_markup : $client->replyKeyboardHide(
				selective : true,
			),
			entities : array(
				$client->messageEntityUnknown(
					offset : 84,
					length : 77,
				),
				$client->messageEntityMention(
					offset : 79,
					length : 47,
				),
				$client->messageEntityHashtag(
					offset : 81,
					length : 31,
				),
				$client->messageEntityBotCommand(
					offset : 44,
					length : 82,
				),
				$client->messageEntityUrl(
					offset : 2,
					length : 7,
				),
				$client->messageEntityEmail(
					offset : 80,
					length : 92,
				),
				$client->messageEntityBold(
					offset : 7,
					length : 9,
				),
				$client->messageEntityItalic(
					offset : 2,
					length : 19,
				),
				$client->messageEntityCode(
					offset : 73,
					length : 45,
				),
				$client->messageEntityPre(
					offset : 69,
					length : 64,
					language : 'HMNqYEKkBfXhuD2m',
				),
				$client->messageEntityTextUrl(
					offset : 52,
					length : 31,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 28,
					length : 20,
					user_id : -6549859101461429180,
				),
				$client->inputMessageEntityMentionName(
					offset : 53,
					length : 97,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 26,
					length : 68,
				),
				$client->messageEntityCashtag(
					offset : 22,
					length : 54,
				),
				$client->messageEntityUnderline(
					offset : 21,
					length : 40,
				),
				$client->messageEntityStrike(
					offset : 46,
					length : 63,
				),
				$client->messageEntityBankCard(
					offset : 75,
					length : 21,
				),
				$client->messageEntitySpoiler(
					offset : 85,
					length : 47,
				),
				$client->messageEntityCustomEmoji(
					offset : 97,
					length : 71,
					document_id : -1169876799714586850,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 98,
					length : 7,
				),
			),
			views : 40,
			forwards : 55,
			replies : $client->messageReplies(
				comments : true,
				replies : 51,
				replies_pts : 86,
				recent_repliers : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				channel_id : -3512517018505809440,
				max_id : 35,
				read_max_id : 33,
			),
			edit_date : 10,
			post_author : 'bGs1ImdOF6u4EPKx',
			grouped_id : -4584470517619707055,
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
					platform : 'gLSTBPHCkvFMcGyU',
					reason : 'QHc7rAN5CkGdgy3V',
					text : '2l7Je6nRxD0TUtLA',
				),
			),
			ttl_period : 93,
			quick_reply_shortcut_id : 26,
			effect : -5637381172170883021,
			factcheck : $client->factCheck(
				need_check : true,
				country : 'e3yBn8cYCLZTSwtz',
				text : $client->textWithEntities(...),
				hash : 5094211546254773500,
			),
			report_delivery_until_date : 22,
			paid_message_stars : 8760647739441333150,
			suggested_post : $client->suggestedPost(
				accepted : true,
				rejected : true,
				price : $client->starsAmount(...),
				schedule_date : 60,
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
			id : 80,
			from_id : $client->peerUser(
				user_id : -5385622200052497020,
			),
			peer_id : $client->peerUser(
				user_id : -5097757992792168465,
			),
			saved_peer_id : $client->peerUser(
				user_id : 3207809071228671467,
			),
			reply_to : $client->messageReplyHeader(
				reply_to_scheduled : true,
				forum_topic : true,
				quote : true,
				reply_to_msg_id : 61,
				reply_to_peer_id : $client->peerUser(...),
				reply_from : $client->messageFwdHeader(...),
				reply_media : $client->messageMediaEmpty(...),
				reply_to_top_id : 58,
				quote_text : 'ZdieaDbmxzJSoQBg',
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
				quote_offset : 75,
				todo_item_id : 19,
			),
			date : 82,
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
			ttl_period : 47,
		),
	),
	new_encrypted_messages : array(
		$client->encryptedMessage(
			random_id : -6146133651694729756,
			chat_id : 11,
			date : 21,
			bytes : 'Z?Dj?LiveProtorH??Q',
			file : $client->encryptedFileEmpty(),
		),
		$client->encryptedMessageService(
			random_id : 6671215648851951453,
			chat_id : 9,
			date : 60,
			bytes : 'e6!LiveProtofcV?',
		),
	),
	other_updates : array(
		$client->updateNewMessage(
			message : $client->messageEmpty(
				id : 99,
				peer_id : $client->peerUser(...),
			),
			pts : 1,
			pts_count : 71,
		),
		$client->updateMessageID(
			id : 65,
			random_id : 6318725183153397470,
		),
		$client->updateDeleteMessages(
			messages : array(18),
			pts : 24,
			pts_count : 84,
		),
		$client->updateUserTyping(
			user_id : -5169090015024275510,
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatUserTyping(
			chat_id : -2270668998837106197,
			from_id : $client->peerUser(
				user_id : -8300876728454226312,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatParticipants(
			participants : $client->chatParticipantsForbidden(
				chat_id : 3965950834626100318,
				self_participant : $client->chatParticipant(...),
			),
		),
		$client->updateUserStatus(
			user_id : -5689182372469885875,
			status : $client->userStatusEmpty(),
		),
		$client->updateUserName(
			user_id : 7904023308999154113,
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
			hash : -4619732908776397791,
			date : 88,
			device : 'iVKrqdbLn0UhSpPt',
			location : 'oPlxwJAIy6mgzBvZ',
		),
		$client->updateNewEncryptedMessage(
			message : $client->encryptedMessage(
				random_id : 8623092798219088816,
				chat_id : 77,
				date : 32,
				bytes : 'H??LiveProto?Z?',
				file : $client->encryptedFileEmpty(...),
			),
			qts : 50,
		),
		$client->updateEncryptedChatTyping(
			chat_id : 6,
		),
		$client->updateEncryption(
			chat : $client->encryptedChatEmpty(
				id : 44,
			),
			date : 7,
		),
		$client->updateEncryptedMessagesRead(
			chat_id : 66,
			max_date : 13,
			date : 71,
		),
		$client->updateChatParticipantAdd(
			chat_id : -6676934827430705814,
			user_id : 5668190393025112536,
			inviter_id : 2443171420034273161,
			date : 40,
			version : 83,
		),
		$client->updateChatParticipantDelete(
			chat_id : 1391093741235014356,
			user_id : 1489992560745243290,
			version : 24,
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
					id : 4,
					ip_address : '127.0.0.1',
					port : 30,
					secret : 'wV?LiveProto????',
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
				mute_until : 51,
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
			inbox_date : 42,
			type : 'EXmz94HuJntsyMfR',
			message : 'IcK3bZL4ujArWCSQ',
			media : $client->messageMediaEmpty(),
			entities : array(
				$client->messageEntityUnknown(
					offset : 22,
					length : 99,
				),
				$client->messageEntityMention(
					offset : 16,
					length : 36,
				),
				$client->messageEntityHashtag(
					offset : 91,
					length : 6,
				),
				$client->messageEntityBotCommand(
					offset : 49,
					length : 48,
				),
				$client->messageEntityUrl(
					offset : 74,
					length : 54,
				),
				$client->messageEntityEmail(
					offset : 38,
					length : 89,
				),
				$client->messageEntityBold(
					offset : 82,
					length : 54,
				),
				$client->messageEntityItalic(
					offset : 95,
					length : 44,
				),
				$client->messageEntityCode(
					offset : 27,
					length : 59,
				),
				$client->messageEntityPre(
					offset : 29,
					length : 16,
					language : 'KnLbi3G59lO6Nqps',
				),
				$client->messageEntityTextUrl(
					offset : 76,
					length : 91,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 26,
					length : 90,
					user_id : -4645732034194908766,
				),
				$client->inputMessageEntityMentionName(
					offset : 8,
					length : 19,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 76,
					length : 57,
				),
				$client->messageEntityCashtag(
					offset : 7,
					length : 20,
				),
				$client->messageEntityUnderline(
					offset : 71,
					length : 76,
				),
				$client->messageEntityStrike(
					offset : 44,
					length : 13,
				),
				$client->messageEntityBankCard(
					offset : 49,
					length : 86,
				),
				$client->messageEntitySpoiler(
					offset : 60,
					length : 96,
				),
				$client->messageEntityCustomEmoji(
					offset : 66,
					length : 28,
					document_id : -2117879576517742199,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 30,
					length : 26,
				),
			),
		),
		$client->updatePrivacy(
			key : $client->privacyKeyStatusTimestamp(),
			rules : array(
				$client->privacyValueAllowContacts(),
				$client->privacyValueAllowAll(),
				$client->privacyValueAllowUsers(
					users : array(-2009736485801564423),
				),
				$client->privacyValueDisallowContacts(),
				$client->privacyValueDisallowAll(),
				$client->privacyValueDisallowUsers(
					users : array(-7157776466455934054),
				),
				$client->privacyValueAllowChatParticipants(
					chats : array(4120850764140475500),
				),
				$client->privacyValueDisallowChatParticipants(
					chats : array(6418520809223676390),
				),
				$client->privacyValueAllowCloseFriends(),
				$client->privacyValueAllowPremium(),
				$client->privacyValueAllowBots(),
				$client->privacyValueDisallowBots(),
			),
		),
		$client->updateUserPhone(
			user_id : -604121937960031511,
			phone : '+1234567890',
		),
		$client->updateReadHistoryInbox(
			folder_id : 98,
			peer : $client->peerUser(
				user_id : 3818978701156768448,
			),
			max_id : 99,
			still_unread_count : 36,
			pts : 4,
			pts_count : 88,
		),
		$client->updateReadHistoryOutbox(
			peer : $client->peerUser(
				user_id : 4764186235744573054,
			),
			max_id : 68,
			pts : 40,
			pts_count : 6,
		),
		$client->updateWebPage(
			webpage : $client->webPageEmpty(
				id : 8461477689204880660,
				url : 'https://docs.liveproto.dev',
			),
			pts : 37,
			pts_count : 22,
		),
		$client->updateReadMessagesContents(
			messages : array(84),
			pts : 44,
			pts_count : 99,
			date : 39,
		),
		$client->updateChannelTooLong(
			channel_id : 8315231257223049969,
			pts : 51,
		),
		$client->updateChannel(
			channel_id : -6521173611282002208,
		),
		$client->updateNewChannelMessage(
			message : $client->messageEmpty(
				id : 1,
				peer_id : $client->peerUser(...),
			),
			pts : 53,
			pts_count : 41,
		),
		$client->updateReadChannelInbox(
			folder_id : 2,
			channel_id : 7243063819883860633,
			max_id : 72,
			still_unread_count : 1,
			pts : 20,
		),
		$client->updateDeleteChannelMessages(
			channel_id : -7694852453089262687,
			messages : array(16),
			pts : 53,
			pts_count : 47,
		),
		$client->updateChannelMessageViews(
			channel_id : 2908980034702786590,
			id : 4,
			views : 15,
		),
		$client->updateChatParticipantAdmin(
			chat_id : 8568403721105364847,
			user_id : 9187300620032963502,
			is_admin : $client->boolFalse(),
			version : 16,
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
			order : array(-961397951895092163),
		),
		$client->updateStickerSets(
			masks : true,
			emojis : true,
		),
		$client->updateSavedGifs(),
		$client->updateBotInlineQuery(
			query_id : 460085098141169567,
			user_id : -3831330494669084215,
			query : 'Pjmh92t10dQGO8I6',
			geo : $client->geoPointEmpty(),
			peer_type : $client->inlineQueryPeerTypeSameBotPM(),
			offset : 'hka51sSVvAKZmeIU',
		),
		$client->updateBotInlineSend(
			user_id : -4089754395389467391,
			query : '91jGXZEr3oO4tUC6',
			geo : $client->geoPointEmpty(),
			id : 'Ncd4zb7sxLEAUYqH',
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 28,
				id : -3046360424055318484,
				access_hash : -2163024338644322395,
			),
		),
		$client->updateEditChannelMessage(
			message : $client->messageEmpty(
				id : 47,
				peer_id : $client->peerUser(...),
			),
			pts : 1,
			pts_count : 27,
		),
		$client->updateBotCallbackQuery(
			query_id : 380353792701469773,
			user_id : 5155426152662408699,
			peer : $client->peerUser(
				user_id : -2141582130413975650,
			),
			msg_id : 76,
			chat_instance : 5457842435030511627,
			data : '???lLiveProto??߼\\',
			game_short_name : '7nuoK0V6dBGE3CMv',
		),
		$client->updateEditMessage(
			message : $client->messageEmpty(
				id : 3,
				peer_id : $client->peerUser(...),
			),
			pts : 40,
			pts_count : 40,
		),
		$client->updateInlineBotCallbackQuery(
			query_id : -2515330418486880804,
			user_id : 4765671941204457545,
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 96,
				id : 9069140500745779817,
				access_hash : -3457415380693836565,
			),
			chat_instance : 5496685121276331780,
			data : '??.??LiveProto?Xy??',
			game_short_name : 'HtorcD61OCjK5xpW',
		),
		$client->updateReadChannelOutbox(
			channel_id : -3331614976769801103,
			max_id : 83,
		),
		$client->updateDraftMessage(
			peer : $client->peerUser(
				user_id : 4005128891377480868,
			),
			top_msg_id : 11,
			saved_peer_id : $client->peerUser(
				user_id : -1029722838386053755,
			),
			draft : $client->draftMessageEmpty(
				date : 31,
			),
		),
		$client->updateReadFeaturedStickers(),
		$client->updateRecentStickers(),
		$client->updateConfig(),
		$client->updatePtsChanged(),
		$client->updateChannelWebPage(
			channel_id : 8281273966890296636,
			webpage : $client->webPageEmpty(
				id : 1416186298244773621,
				url : 'https://docs.liveproto.dev',
			),
			pts : 91,
			pts_count : 91,
		),
		$client->updateDialogPinned(
			pinned : true,
			folder_id : 65,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
		),
		$client->updatePinnedDialogs(
			folder_id : 10,
			order : array(
				$client->dialogPeer(
					peer : $client->peerUser(...),
				),
				$client->dialogPeerFolder(
					folder_id : 17,
				),
			),
		),
		$client->updateBotWebhookJSON(
			data : $client->dataJSON(
				data : 'gcGXIjwfE4AByWaK',
			),
		),
		$client->updateBotWebhookJSONQuery(
			query_id : -4569396913007123426,
			data : $client->dataJSON(
				data : 'Xg8lHxuoiFwU5Emn',
			),
			timeout : 34,
		),
		$client->updateBotShippingQuery(
			query_id : 6968940645964150762,
			user_id : 7374826084098667803,
			payload : '???ajLiveProtoy?q??',
			shipping_address : $client->postAddress(
				street_line1 : '4oKVB18AspTSyeNI',
				street_line2 : 'PBVgcu2EehUZkyni',
				city : '8pbK0ifLjdchUPSz',
				state : 'np7lxYcEOehbX83o',
				country_iso2 : 'zDkF8PBWp6OJ0Ljg',
				post_code : 'DsU3aNcxrI2HX7ny',
			),
		),
		$client->updateBotPrecheckoutQuery(
			query_id : -4266893869414525739,
			user_id : -334835011750552333,
			payload : '??Gy6LiveProto7??v?',
			info : $client->paymentRequestedInfo(
				name : 'AtYGXKZheC6WOTmH',
				phone : '+1234567890',
				email : 'reply@liveproto.dev',
				shipping_address : $client->postAddress(...),
			),
			shipping_option_id : 'rOFJ2e9ayhYCkXLA',
			currency : 'qcPVQ2LMjeB1an47',
			total_amount : -4919044074650917457,
		),
		$client->updatePhoneCall(
			phone_call : $client->phoneCallEmpty(
				id : -1221946745828072294,
			),
		),
		$client->updateLangPackTooLong(
			lang_code : 'x4fbv8Z6h0LPB3a1',
		),
		$client->updateLangPack(
			difference : $client->langPackDifference(
				lang_code : 'tN528ivy0ZToVQA7',
				from_version : 46,
				version : 11,
				strings : array(
					$client->langPackString(...),
					$client->langPackStringPluralized(...),
					$client->langPackStringDeleted(...),
				),
			),
		),
		$client->updateFavedStickers(),
		$client->updateChannelReadMessagesContents(
			channel_id : 2514228934601640747,
			top_msg_id : 86,
			saved_peer_id : $client->peerUser(
				user_id : 7918156725647070223,
			),
			messages : array(18),
		),
		$client->updateContactsReset(),
		$client->updateChannelAvailableMessages(
			channel_id : 4957823587376483242,
			available_min_id : 98,
		),
		$client->updateDialogUnreadMark(
			unread : true,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
			saved_peer_id : $client->peerUser(
				user_id : 8181915055282314923,
			),
		),
		$client->updateMessagePoll(
			poll_id : 2535179804939763162,
			poll : $client->poll(
				id : -5711261080247189359,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 93,
				close_date : 99,
			),
			results : $client->pollResults(
				min : true,
				results : array(
					$client->pollAnswerVoters(...),
				),
				total_voters : 8,
				recent_voters : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				solution : 'mJaXo21wRCqxzvj8',
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
				user_id : -3557544515489711364,
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
				until_date : 50,
			),
			version : 88,
		),
		$client->updateFolderPeers(
			folder_peers : array(
				$client->folderPeer(
					peer : $client->peerUser(...),
					folder_id : 70,
				),
			),
			pts : 34,
			pts_count : 86,
		),
		$client->updatePeerSettings(
			peer : $client->peerUser(
				user_id : -35501721056957110,
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
				geo_distance : 35,
				request_chat_title : 'AcilRrpEz3kK41dU',
				request_chat_date : 50,
				business_bot_id : 3225234049858794723,
				business_bot_manage_url : 'https://docs.liveproto.dev',
				charge_paid_message_stars : 6073946072991528510,
				registration_month : 'esyqYWp54j7AMgvN',
				phone_country : '+1234567890',
				name_change_date : 74,
				photo_change_date : 86,
			),
		),
		$client->updatePeerLocated(
			peers : array(
				$client->peerLocated(
					peer : $client->peerUser(...),
					expires : 70,
					distance : 91,
				),
				$client->peerSelfLocated(
					expires : 50,
				),
			),
		),
		$client->updateNewScheduledMessage(
			message : $client->messageEmpty(
				id : 35,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteScheduledMessages(
			peer : $client->peerUser(
				user_id : 499778127872224950,
			),
			messages : array(31),
			sent_messages : array(61),
		),
		$client->updateTheme(
			theme : $client->theme(
				creator : true,
				default : true,
				for_chat : true,
				id : 2058156457702042433,
				access_hash : 4148932740698310069,
				slug : 'oFTKPqhMVQzpylgs',
				title : 'ZxUim6OW9PNTlLtB',
				document : $client->documentEmpty(...),
				settings : array(
					$client->themeSettings(...),
				),
				emoticon : '5a3TvoNIwL0StfUb',
				installs_count : 20,
			),
		),
		$client->updateGeoLiveViewed(
			peer : $client->peerUser(
				user_id : -8537326709400762213,
			),
			msg_id : 33,
		),
		$client->updateLoginToken(),
		$client->updateMessagePollVote(
			poll_id : -579678351939437218,
			peer : $client->peerUser(
				user_id : 2934016617353495761,
			),
			options : array('??nVLiveProto	??V'),
			qts : 24,
		),
		$client->updateDialogFilter(
			id : 34,
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
				id : 77,
				title : $client->textWithEntities(...),
				emoticon : '1lut4YvqJLNA7MHZ',
				color : 70,
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
			order : array(17),
		),
		$client->updateDialogFilters(),
		$client->updatePhoneCallSignalingData(
			phone_call_id : -681300597810365643,
			data : 'I?glgLiveProto????|',
		),
		$client->updateChannelMessageForwards(
			channel_id : -5170737353530665862,
			id : 26,
			forwards : 87,
		),
		$client->updateReadChannelDiscussionInbox(
			channel_id : 8975902863629059004,
			top_msg_id : 54,
			read_max_id : 74,
			broadcast_id : -260603281955170393,
			broadcast_post : 18,
		),
		$client->updateReadChannelDiscussionOutbox(
			channel_id : 1137357894822039304,
			top_msg_id : 96,
			read_max_id : 93,
		),
		$client->updatePeerBlocked(
			blocked : true,
			blocked_my_stories_from : true,
			peer_id : $client->peerUser(
				user_id : -5152260784421749782,
			),
		),
		$client->updateChannelUserTyping(
			channel_id : -680551122384604837,
			top_msg_id : 71,
			from_id : $client->peerUser(
				user_id : 6031247736785308408,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updatePinnedMessages(
			pinned : true,
			peer : $client->peerUser(
				user_id : -4117942768063314106,
			),
			messages : array(26),
			pts : 53,
			pts_count : 41,
		),
		$client->updatePinnedChannelMessages(
			pinned : true,
			channel_id : -6247361242913307480,
			messages : array(3),
			pts : 44,
			pts_count : 63,
		),
		$client->updateChat(
			chat_id : -8134061635003811889,
		),
		$client->updateGroupCallParticipants(
			call : $client->inputGroupCall(
				id : 2447060375158605549,
				access_hash : 5708494588514539803,
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
					date : 18,
					active_date : 76,
					source : 47,
					volume : 76,
					about : 'ztnmZeRgHPKuQC72',
					raise_hand_rating : -1654916621211306381,
					video : $client->groupCallParticipantVideo(...),
					presentation : $client->groupCallParticipantVideo(...),
				),
			),
			version : 45,
		),
		$client->updateGroupCall(
			chat_id : 7073192679577155297,
			call : $client->groupCallDiscarded(
				id : -1834067011647345477,
				access_hash : -7520320261445698208,
				duration : 13,
			),
		),
		$client->updatePeerHistoryTTL(
			peer : $client->peerUser(
				user_id : -8515480816577036192,
			),
			ttl_period : 79,
		),
		$client->updateChatParticipant(
			chat_id : -8607443343427079634,
			date : 10,
			actor_id : -6141931754670237473,
			user_id : 6075975244826345001,
			prev_participant : $client->chatParticipant(
				user_id : 7237869989629272329,
				inviter_id : -3764957687759263226,
				date : 71,
			),
			new_participant : $client->chatParticipant(
				user_id : 2959251937274295219,
				inviter_id : 1889630326479672812,
				date : 96,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : '5MfhGVrio20NjHWE',
				admin_id : -4708316358378592560,
				date : 85,
				start_date : 21,
				expire_date : 89,
				usage_limit : 21,
				usage : 61,
				requested : 4,
				subscription_expired : 44,
				title : 'yDrYE86IcK31Nnmw',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 68,
		),
		$client->updateChannelParticipant(
			via_chatlist : true,
			channel_id : 4378677807687324310,
			date : 56,
			actor_id : 717124533897597899,
			user_id : -3932703873120691814,
			prev_participant : $client->channelParticipant(
				user_id : -7750726723970276104,
				date : 90,
				subscription_until_date : 64,
			),
			new_participant : $client->channelParticipant(
				user_id : -7853339051063762041,
				date : 64,
				subscription_until_date : 98,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'reuaIdTPV4zm3MZO',
				admin_id : -7510793855298424337,
				date : 11,
				start_date : 72,
				expire_date : 0,
				usage_limit : 67,
				usage : 55,
				requested : 65,
				subscription_expired : 68,
				title : 'c8RphmlgxOdAZrGD',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 1,
		),
		$client->updateBotStopped(
			user_id : 7427501154836638192,
			date : 50,
			stopped : $client->boolFalse(),
			qts : 72,
		),
		$client->updateGroupCallConnection(
			presentation : true,
			params : $client->dataJSON(
				data : 'dsr6x4ZvDyhuH2bR',
			),
		),
		$client->updateBotCommands(
			peer : $client->peerUser(
				user_id : 6296484783835295388,
			),
			bot_id : 8019708366374591163,
			commands : array(
				$client->botCommand(
					command : 'torniPwplIQFuGy3',
					description : 'ehCVkSt08XnxF1id',
				),
			),
		),
		$client->updatePendingJoinRequests(
			peer : $client->peerUser(
				user_id : -3801390493407008979,
			),
			requests_pending : 49,
			recent_requesters : array(-1689842006946458343),
		),
		$client->updateBotChatInviteRequester(
			peer : $client->peerUser(
				user_id : -3004546156668634433,
			),
			date : 25,
			user_id : -1261250017599064875,
			about : 'e5OgNAnR2VJawhSb',
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : '7c5NLyp3Hz2lPMWu',
				admin_id : -4359149165703526465,
				date : 51,
				start_date : 75,
				expire_date : 93,
				usage_limit : 98,
				usage : 86,
				requested : 45,
				subscription_expired : 72,
				title : 'Y8sQhvKGyXtPaWRV',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 14,
		),
		$client->updateMessageReactions(
			peer : $client->peerUser(
				user_id : -4362155464449042527,
			),
			msg_id : 40,
			top_msg_id : 57,
			saved_peer_id : $client->peerUser(
				user_id : 2199220724653001559,
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
			query_id : -9211571290997712070,
		),
		$client->updateBotMenuButton(
			bot_id : 2799996276709015373,
			button : $client->botMenuButtonDefault(),
		),
		$client->updateSavedRingtones(),
		$client->updateTranscribedAudio(
			pending : true,
			peer : $client->peerUser(
				user_id : -6431530809913728715,
			),
			msg_id : 75,
			transcription_id : 4181522856099445953,
			text : 'VOxMjQFDPqtgNKX0',
		),
		$client->updateReadFeaturedEmojiStickers(),
		$client->updateUserEmojiStatus(
			user_id : -8807844768216361900,
			emoji_status : $client->emojiStatusEmpty(),
		),
		$client->updateRecentEmojiStatuses(),
		$client->updateRecentReactions(),
		$client->updateMoveStickerSetToTop(
			masks : true,
			emojis : true,
			stickerset : -8803222477504179021,
		),
		$client->updateMessageExtendedMedia(
			peer : $client->peerUser(
				user_id : -6786834250454338973,
			),
			msg_id : 14,
			extended_media : array(
				$client->messageExtendedMediaPreview(
					w : 57,
					h : 79,
					thumb : $client->photoSizeEmpty(...),
					video_duration : 81,
				),
				$client->messageExtendedMedia(
					media : $client->messageMediaEmpty(...),
				),
			),
		),
		$client->updateChannelPinnedTopic(
			pinned : true,
			channel_id : 8466468269001567193,
			topic_id : 50,
		),
		$client->updateChannelPinnedTopics(
			channel_id : 6808465090607864659,
			order : array(4),
		),
		$client->updateUser(
			user_id : -4600553200835874846,
		),
		$client->updateAutoSaveSettings(),
		$client->updateStory(
			peer : $client->peerUser(
				user_id : -6240995389643560452,
			),
			story : $client->storyItemDeleted(
				id : 84,
			),
		),
		$client->updateReadStories(
			peer : $client->peerUser(
				user_id : -1588035796515914763,
			),
			max_id : 9,
		),
		$client->updateStoryID(
			id : 68,
			random_id : -2852744236904001253,
		),
		$client->updateStoriesStealthMode(
			stealth_mode : $client->storiesStealthMode(
				active_until_date : 43,
				cooldown_until_date : 90,
			),
		),
		$client->updateSentStoryReaction(
			peer : $client->peerUser(
				user_id : 7246332666972375708,
			),
			story_id : 2,
			reaction : $client->reactionEmpty(),
		),
		$client->updateBotChatBoost(
			peer : $client->peerUser(
				user_id : -1090291291668701156,
			),
			boost : $client->boost(
				gift : true,
				giveaway : true,
				unclaimed : true,
				id : 'ZebD2ljMV8LHmW05',
				user_id : -1899227754421516078,
				giveaway_msg_id : 75,
				date : 93,
				expires : 30,
				used_gift_slug : 's4Iv5Cl0iPxK32tY',
				multiplier : 12,
				stars : 8879644455518744282,
			),
			qts : 58,
		),
		$client->updateChannelViewForumAsMessages(
			channel_id : -4376227050932789445,
			enabled : $client->boolFalse(),
		),
		$client->updatePeerWallpaper(
			wallpaper_overridden : true,
			peer : $client->peerUser(
				user_id : -1112845141765543079,
			),
			wallpaper : $client->wallPaper(
				id : -6149889963401997209,
				creator : true,
				default : true,
				pattern : true,
				dark : true,
				access_hash : 21578007930116777,
				slug : 'BOh05CDnsbJMNvaz',
				document : $client->documentEmpty(...),
				settings : $client->wallPaperSettings(...),
			),
		),
		$client->updateBotMessageReaction(
			peer : $client->peerUser(
				user_id : 6150927346337373745,
			),
			msg_id : 13,
			date : 50,
			actor : $client->peerUser(
				user_id : -8525697014366577062,
			),
			old_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'DY18NgLQimJcuf4k',
				),
				$client->reactionCustomEmoji(
					document_id : -1844331194659608897,
				),
				$client->reactionPaid(),
			),
			new_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'P5U7OJqcLEmVu1Za',
				),
				$client->reactionCustomEmoji(
					document_id : -4945417095489612025,
				),
				$client->reactionPaid(),
			),
			qts : 43,
		),
		$client->updateBotMessageReactions(
			peer : $client->peerUser(
				user_id : 2419095098705196372,
			),
			msg_id : 74,
			date : 52,
			reactions : array(
				$client->reactionCount(
					chosen_order : 17,
					reaction : $client->reactionEmpty(...),
					count : 80,
				),
			),
			qts : 91,
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
					folder_id : 65,
				),
			),
		),
		$client->updateSavedReactionTags(),
		$client->updateSmsJob(
			job_id : 'XDdY1PViMr0c6TO5',
		),
		$client->updateQuickReplies(
			quick_replies : array(
				$client->quickReply(
					shortcut_id : 3,
					shortcut : 'aethYWQk4EIvdOsp',
					top_message : 58,
					count : 90,
				),
			),
		),
		$client->updateNewQuickReply(
			quick_reply : $client->quickReply(
				shortcut_id : 86,
				shortcut : '1aBycgOFP9Im5TEj',
				top_message : 37,
				count : 91,
			),
		),
		$client->updateDeleteQuickReply(
			shortcut_id : 39,
		),
		$client->updateQuickReplyMessage(
			message : $client->messageEmpty(
				id : 56,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteQuickReplyMessages(
			shortcut_id : 30,
			messages : array(84),
		),
		$client->updateBotBusinessConnect(
			connection : $client->botBusinessConnection(
				disabled : true,
				connection_id : 'Qws3ukXtHfZJWvSF',
				user_id : 1874762223938061195,
				dc_id : 92,
				date : 82,
				rights : $client->businessBotRights(...),
			),
			qts : 100,
		),
		$client->updateBotNewBusinessMessage(
			connection_id : 'fvK8S6xormywIGjQ',
			message : $client->messageEmpty(
				id : 75,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 100,
				peer_id : $client->peerUser(...),
			),
			qts : 87,
		),
		$client->updateBotEditBusinessMessage(
			connection_id : 'TacP0AYosZ9tXrkF',
			message : $client->messageEmpty(
				id : 75,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 44,
				peer_id : $client->peerUser(...),
			),
			qts : 17,
		),
		$client->updateBotDeleteBusinessMessage(
			connection_id : 'oT1v6tRmgIKz0bdG',
			peer : $client->peerUser(
				user_id : 6989046298568419018,
			),
			messages : array(59),
			qts : 7,
		),
		$client->updateNewStoryReaction(
			story_id : 88,
			peer : $client->peerUser(
				user_id : 3557286111968013781,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->updateStarsBalance(
			balance : $client->starsAmount(
				amount : 4427949554543190899,
				nanos : 52,
			),
		),
		$client->updateBusinessBotCallbackQuery(
			query_id : -6065419241497919637,
			user_id : -1566996603320706840,
			connection_id : 'rLYlUwJG0XSokt17',
			message : $client->messageEmpty(
				id : 57,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 35,
				peer_id : $client->peerUser(...),
			),
			chat_instance : 2796090232990058973,
			data : '???!LiveProto???',
		),
		$client->updateStarsRevenueStatus(
			peer : $client->peerUser(
				user_id : -7340503936220440975,
			),
			status : $client->starsRevenueStatus(
				withdrawal_enabled : true,
				current_balance : $client->starsAmount(...),
				available_balance : $client->starsAmount(...),
				overall_revenue : $client->starsAmount(...),
				next_withdrawal_at : 9,
			),
		),
		$client->updateBotPurchasedPaidMedia(
			user_id : 5529220909795189994,
			payload : 'TnLcg1x8HW3RVdXE',
			qts : 59,
		),
		$client->updatePaidReactionPrivacy(
			private : $client->paidReactionPrivacyDefault(),
		),
		$client->updateSentPhoneCode(
			sent_code : $client->auth->sentCode(
				type : $client->auth->sentCodeTypeApp(...),
				phone_code_hash : '+1234567890',
				next_type : $client->auth->codeTypeSms(...),
				timeout : 57,
			),
		),
		$client->updateGroupCallChainBlocks(
			call : $client->inputGroupCall(
				id : -1686324194672328860,
				access_hash : 3116359992704490898,
			),
			sub_chain_id : 39,
			blocks : array('j/-?LiveProto???̊'),
			next_offset : 94,
		),
		$client->updateReadMonoForumInbox(
			channel_id : 1395915094918266955,
			saved_peer_id : $client->peerUser(
				user_id : 3240676680684871627,
			),
			read_max_id : 64,
		),
		$client->updateReadMonoForumOutbox(
			channel_id : -4322536443924290394,
			saved_peer_id : $client->peerUser(
				user_id : -7797352359084115738,
			),
			read_max_id : 82,
		),
		$client->updateMonoForumNoPaidException(
			exception : true,
			channel_id : 1664772422954053304,
			saved_peer_id : $client->peerUser(
				user_id : 8118334855967636149,
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -3107436583552730477,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -8265760368249168160,
			title : 'gRf4d5AYHoxQszvE',
			photo : $client->chatPhotoEmpty(),
			participants_count : 67,
			date : 66,
			version : 16,
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
				until_date : 69,
			),
		),
		$client->chatForbidden(
			id : 3991507576301742142,
			title : '405sMztBT3n8EYPo',
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
			id : -6859469394673959550,
			access_hash : -7754583380743522988,
			title : 'w1hSqrg3adpRJWnf',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 60,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'JcK4F2QCLNZwtmSi',
					reason : 'dJ4GTKXazUSLhZC0',
					text : 'ADrcEpLvuCo1wlB5',
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
				until_date : 19,
			),
			participants_count : 98,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 61,
			color : $client->peerColor(
				color : 98,
				background_emoji_id : 2554951958641738260,
			),
			profile_color : $client->peerColor(
				color : 55,
				background_emoji_id : -3506066016327893080,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 76,
			subscription_until_date : 72,
			bot_verification_icon : 8458393294765730739,
			send_paid_messages_stars : 9008026750224519717,
			linked_monoforum_id : 3850492071011451214,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 887720830145027177,
			access_hash : -4663266661574631020,
			title : 'mUpljnP9fqhHWBMV',
			until_date : 72,
		),
	),
	users : array(
		$client->userEmpty(
			id : -4024154719384789511,
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
			id : -2043201976854917363,
			access_hash : -6027401629317792600,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 27,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '6xhWzS4VECXGuZ1Q',
					reason : 'DHcLQIJ2F6ot8VnZ',
					text : 'iyYkQgKVFICjxMfB',
				),
			),
			bot_inline_placeholder : 'KRyB0JdMDtUki7qQ',
			lang_code : 'uUr2CodbsRn5kBHV',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 29,
			color : $client->peerColor(
				color : 19,
				background_emoji_id : 4238985981808997907,
			),
			profile_color : $client->peerColor(
				color : 94,
				background_emoji_id : -1639375818671800901,
			),
			bot_active_users : 24,
			bot_verification_icon : -3779750845317247955,
			send_paid_messages_stars : -4175090180550200099,
		),
	),
	intermediate_state : $client->updates->state(
		pts : 43,
		qts : 93,
		date : 32,
		seq : 69,
		unread_count : 62,
	),
);
```