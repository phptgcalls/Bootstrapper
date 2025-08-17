# updates.channelDifference

**Description** : *The new updates*

**Layer** : 211

```tl
updates.channelDifference#2064674e flags:# final:flags.0?true pts:int timeout:flags.1?int new_messages:Vector<Message> other_updates:Vector<Update> chats:Vector<Chat> users:Vector<User> = updates.ChannelDifference;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **final** | [`flags.0?true`](type/true) | Whether there are more updates to be fetched using getDifference, starting from the provided pts |
| <mark>pts</mark> | [`int`](type/int) | The PTS from which to start getting updates the next time |
| **timeout** | [`flags.1?int`](type/int) | Clients are supposed to refetch the channel difference after timeout seconds have elapsed, if the user is currently viewing the chat, see here » for more info |
| <mark>new_messages</mark> | [`Vector<Message>`](type/Message) | New messages |
| <mark>other_updates</mark> | [`Vector<Update>`](type/Update) | Other updates |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users |

---

## Type

[updates.ChannelDifference](type/updates.ChannelDifference)

---

## Example

```php
$updatesChannelDifference = $client->updates->channelDifference(
	final : true,
	pts : 90,
	timeout : 30,
	new_messages : array(
		$client->messageEmpty(
			id : 71,
			peer_id : $client->peerUser(
				user_id : -2396515335207025080,
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
			id : 34,
			from_id : $client->peerUser(
				user_id : 5827011299243990201,
			),
			from_boosts_applied : 64,
			peer_id : $client->peerUser(
				user_id : 7679108578865966764,
			),
			saved_peer_id : $client->peerUser(
				user_id : 2076451724738218093,
			),
			fwd_from : $client->messageFwdHeader(
				imported : true,
				saved_out : true,
				from_id : $client->peerUser(...),
				from_name : 'femNPt0Dhcp2KFiU',
				date : 19,
				channel_post : 97,
				post_author : 'oE9s4b7JXxcaFIHi',
				saved_from_peer : $client->peerUser(...),
				saved_from_msg_id : 7,
				saved_from_id : $client->peerUser(...),
				saved_from_name : '2FkvV0bPnQMiB4Of',
				saved_date : 61,
				psa_type : 'v1LlJydEmVcBsGKQ',
			),
			via_bot_id : 3054224279507383000,
			via_business_bot_id : 5173664530480398560,
			reply_to : $client->messageReplyHeader(
				reply_to_scheduled : true,
				forum_topic : true,
				quote : true,
				reply_to_msg_id : 40,
				reply_to_peer_id : $client->peerUser(...),
				reply_from : $client->messageFwdHeader(...),
				reply_media : $client->messageMediaEmpty(...),
				reply_to_top_id : 82,
				quote_text : 'y4MQUHqDFRNWThs6',
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
				quote_offset : 47,
				todo_item_id : 45,
			),
			date : 59,
			message : 'q93QS2ethk8JVvGm',
			media : $client->messageMediaEmpty(),
			reply_markup : $client->replyKeyboardHide(
				selective : true,
			),
			entities : array(
				$client->messageEntityUnknown(
					offset : 68,
					length : 13,
				),
				$client->messageEntityMention(
					offset : 50,
					length : 9,
				),
				$client->messageEntityHashtag(
					offset : 23,
					length : 65,
				),
				$client->messageEntityBotCommand(
					offset : 45,
					length : 5,
				),
				$client->messageEntityUrl(
					offset : 58,
					length : 63,
				),
				$client->messageEntityEmail(
					offset : 75,
					length : 70,
				),
				$client->messageEntityBold(
					offset : 56,
					length : 95,
				),
				$client->messageEntityItalic(
					offset : 50,
					length : 3,
				),
				$client->messageEntityCode(
					offset : 99,
					length : 47,
				),
				$client->messageEntityPre(
					offset : 23,
					length : 86,
					language : 'pjGBcASDJWmPU3Er',
				),
				$client->messageEntityTextUrl(
					offset : 79,
					length : 20,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 53,
					length : 12,
					user_id : -8174140243725777018,
				),
				$client->inputMessageEntityMentionName(
					offset : 90,
					length : 13,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 11,
					length : 33,
				),
				$client->messageEntityCashtag(
					offset : 86,
					length : 20,
				),
				$client->messageEntityUnderline(
					offset : 96,
					length : 26,
				),
				$client->messageEntityStrike(
					offset : 36,
					length : 39,
				),
				$client->messageEntityBankCard(
					offset : 92,
					length : 11,
				),
				$client->messageEntitySpoiler(
					offset : 29,
					length : 47,
				),
				$client->messageEntityCustomEmoji(
					offset : 62,
					length : 57,
					document_id : 8859235801749551962,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 46,
					length : 90,
				),
			),
			views : 92,
			forwards : 3,
			replies : $client->messageReplies(
				comments : true,
				replies : 86,
				replies_pts : 40,
				recent_repliers : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				channel_id : -4083711665551332794,
				max_id : 2,
				read_max_id : 86,
			),
			edit_date : 15,
			post_author : 'M682ZwI5STstEh4c',
			grouped_id : 1250833578225599644,
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
					platform : 'dq4F57vn0XIBj9NZ',
					reason : 'HW3Da2ZlM7AVfvER',
					text : 'X4NeI3GghLHYyVW1',
				),
			),
			ttl_period : 90,
			quick_reply_shortcut_id : 15,
			effect : -1286446590626301101,
			factcheck : $client->factCheck(
				need_check : true,
				country : 'cEQHOeJ754uP0CYl',
				text : $client->textWithEntities(...),
				hash : -2361125312195876012,
			),
			report_delivery_until_date : 44,
			paid_message_stars : 5153206156378386800,
			suggested_post : $client->suggestedPost(
				accepted : true,
				rejected : true,
				price : $client->starsAmount(...),
				schedule_date : 40,
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
			id : 16,
			from_id : $client->peerUser(
				user_id : -1777058951341964606,
			),
			peer_id : $client->peerUser(
				user_id : -2553908684816286358,
			),
			saved_peer_id : $client->peerUser(
				user_id : 3388210128300782447,
			),
			reply_to : $client->messageReplyHeader(
				reply_to_scheduled : true,
				forum_topic : true,
				quote : true,
				reply_to_msg_id : 37,
				reply_to_peer_id : $client->peerUser(...),
				reply_from : $client->messageFwdHeader(...),
				reply_media : $client->messageMediaEmpty(...),
				reply_to_top_id : 68,
				quote_text : 'J6aK98OjPUodDCTI',
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
				quote_offset : 73,
				todo_item_id : 50,
			),
			date : 4,
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
			ttl_period : 50,
		),
	),
	other_updates : array(
		$client->updateNewMessage(
			message : $client->messageEmpty(
				id : 12,
				peer_id : $client->peerUser(...),
			),
			pts : 17,
			pts_count : 62,
		),
		$client->updateMessageID(
			id : 27,
			random_id : -6057077048570352129,
		),
		$client->updateDeleteMessages(
			messages : array(24),
			pts : 42,
			pts_count : 96,
		),
		$client->updateUserTyping(
			user_id : -2628762054992706712,
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatUserTyping(
			chat_id : -2345698164490529437,
			from_id : $client->peerUser(
				user_id : -8430600979711923971,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updateChatParticipants(
			participants : $client->chatParticipantsForbidden(
				chat_id : 548770254192277339,
				self_participant : $client->chatParticipant(...),
			),
		),
		$client->updateUserStatus(
			user_id : -4794507916537490819,
			status : $client->userStatusEmpty(),
		),
		$client->updateUserName(
			user_id : 8958467603428279565,
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
			hash : 2837833895668816001,
			date : 63,
			device : 'zNUdV4iI7mQY5wq6',
			location : '7DFuLxUMNogPeRJm',
		),
		$client->updateNewEncryptedMessage(
			message : $client->encryptedMessage(
				random_id : 3646369354484602447,
				chat_id : 42,
				date : 72,
				bytes : '?֛pLiveProto?QY?',
				file : $client->encryptedFileEmpty(...),
			),
			qts : 54,
		),
		$client->updateEncryptedChatTyping(
			chat_id : 2,
		),
		$client->updateEncryption(
			chat : $client->encryptedChatEmpty(
				id : 17,
			),
			date : 81,
		),
		$client->updateEncryptedMessagesRead(
			chat_id : 35,
			max_date : 16,
			date : 46,
		),
		$client->updateChatParticipantAdd(
			chat_id : -1858669024248327168,
			user_id : -3994428469644824917,
			inviter_id : 8577192618763446082,
			date : 68,
			version : 46,
		),
		$client->updateChatParticipantDelete(
			chat_id : -8558902889289216835,
			user_id : -7686512805259814508,
			version : 62,
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
					port : 31,
					secret : 'C9qX=LiveProto<???',
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
				mute_until : 33,
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
			inbox_date : 79,
			type : 'PJ5RgDB2NvurxpWM',
			message : 'xiIlQybNJaAkHqRO',
			media : $client->messageMediaEmpty(),
			entities : array(
				$client->messageEntityUnknown(
					offset : 63,
					length : 98,
				),
				$client->messageEntityMention(
					offset : 91,
					length : 99,
				),
				$client->messageEntityHashtag(
					offset : 58,
					length : 77,
				),
				$client->messageEntityBotCommand(
					offset : 40,
					length : 48,
				),
				$client->messageEntityUrl(
					offset : 37,
					length : 11,
				),
				$client->messageEntityEmail(
					offset : 19,
					length : 3,
				),
				$client->messageEntityBold(
					offset : 5,
					length : 30,
				),
				$client->messageEntityItalic(
					offset : 66,
					length : 80,
				),
				$client->messageEntityCode(
					offset : 88,
					length : 45,
				),
				$client->messageEntityPre(
					offset : 94,
					length : 15,
					language : '1a36LkcpIiRv0DJX',
				),
				$client->messageEntityTextUrl(
					offset : 96,
					length : 77,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 24,
					length : 8,
					user_id : 7878765992644084195,
				),
				$client->inputMessageEntityMentionName(
					offset : 49,
					length : 11,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 9,
					length : 75,
				),
				$client->messageEntityCashtag(
					offset : 84,
					length : 93,
				),
				$client->messageEntityUnderline(
					offset : 68,
					length : 24,
				),
				$client->messageEntityStrike(
					offset : 56,
					length : 32,
				),
				$client->messageEntityBankCard(
					offset : 49,
					length : 74,
				),
				$client->messageEntitySpoiler(
					offset : 12,
					length : 56,
				),
				$client->messageEntityCustomEmoji(
					offset : 99,
					length : 1,
					document_id : 5348036409635897253,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 79,
					length : 95,
				),
			),
		),
		$client->updatePrivacy(
			key : $client->privacyKeyStatusTimestamp(),
			rules : array(
				$client->privacyValueAllowContacts(),
				$client->privacyValueAllowAll(),
				$client->privacyValueAllowUsers(
					users : array(-114634463151587712),
				),
				$client->privacyValueDisallowContacts(),
				$client->privacyValueDisallowAll(),
				$client->privacyValueDisallowUsers(
					users : array(2844684786936652575),
				),
				$client->privacyValueAllowChatParticipants(
					chats : array(5313321474976553952),
				),
				$client->privacyValueDisallowChatParticipants(
					chats : array(-6889273812373328897),
				),
				$client->privacyValueAllowCloseFriends(),
				$client->privacyValueAllowPremium(),
				$client->privacyValueAllowBots(),
				$client->privacyValueDisallowBots(),
			),
		),
		$client->updateUserPhone(
			user_id : 4637701804169945465,
			phone : '+1234567890',
		),
		$client->updateReadHistoryInbox(
			folder_id : 82,
			peer : $client->peerUser(
				user_id : 1985309979125381780,
			),
			max_id : 6,
			still_unread_count : 28,
			pts : 54,
			pts_count : 46,
		),
		$client->updateReadHistoryOutbox(
			peer : $client->peerUser(
				user_id : -6950993234308667847,
			),
			max_id : 56,
			pts : 95,
			pts_count : 27,
		),
		$client->updateWebPage(
			webpage : $client->webPageEmpty(
				id : 220726567598613761,
				url : 'https://docs.liveproto.dev',
			),
			pts : 4,
			pts_count : 20,
		),
		$client->updateReadMessagesContents(
			messages : array(71),
			pts : 70,
			pts_count : 11,
			date : 75,
		),
		$client->updateChannelTooLong(
			channel_id : -6928850465032759178,
			pts : 18,
		),
		$client->updateChannel(
			channel_id : 1317972215997917288,
		),
		$client->updateNewChannelMessage(
			message : $client->messageEmpty(
				id : 66,
				peer_id : $client->peerUser(...),
			),
			pts : 50,
			pts_count : 65,
		),
		$client->updateReadChannelInbox(
			folder_id : 71,
			channel_id : -9034356130633579006,
			max_id : 79,
			still_unread_count : 46,
			pts : 92,
		),
		$client->updateDeleteChannelMessages(
			channel_id : 2607987316137638253,
			messages : array(87),
			pts : 76,
			pts_count : 87,
		),
		$client->updateChannelMessageViews(
			channel_id : 3643009772392985939,
			id : 59,
			views : 44,
		),
		$client->updateChatParticipantAdmin(
			chat_id : 2716885543300567643,
			user_id : -5832618632436127434,
			is_admin : $client->boolFalse(),
			version : 57,
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
			order : array(-2633990164694772909),
		),
		$client->updateStickerSets(
			masks : true,
			emojis : true,
		),
		$client->updateSavedGifs(),
		$client->updateBotInlineQuery(
			query_id : -6889684347209170263,
			user_id : 5649722121830926031,
			query : 'e7zADTGjbZrVpY2u',
			geo : $client->geoPointEmpty(),
			peer_type : $client->inlineQueryPeerTypeSameBotPM(),
			offset : 'cJQXKluAeidjU7IG',
		),
		$client->updateBotInlineSend(
			user_id : 151835149759003156,
			query : 'z8F1DPjNoucvw6m0',
			geo : $client->geoPointEmpty(),
			id : '7NJmdEx8L0qtpRHW',
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 34,
				id : -416171566860883820,
				access_hash : 4683133536156483680,
			),
		),
		$client->updateEditChannelMessage(
			message : $client->messageEmpty(
				id : 68,
				peer_id : $client->peerUser(...),
			),
			pts : 73,
			pts_count : 6,
		),
		$client->updateBotCallbackQuery(
			query_id : -2501065268293832538,
			user_id : 8554306443297246568,
			peer : $client->peerUser(
				user_id : 3693990608098367650,
			),
			msg_id : 8,
			chat_instance : -1325796977114223522,
			data : '?"?k?LiveProto\'m??f',
			game_short_name : 'hG2vOJEmQxZpizY5',
		),
		$client->updateEditMessage(
			message : $client->messageEmpty(
				id : 6,
				peer_id : $client->peerUser(...),
			),
			pts : 57,
			pts_count : 15,
		),
		$client->updateInlineBotCallbackQuery(
			query_id : -3693794653774753126,
			user_id : 4879058962556863241,
			msg_id : $client->inputBotInlineMessageID(
				dc_id : 22,
				id : -6171822469493343118,
				access_hash : -7137533921188004228,
			),
			chat_instance : -3111901712796021165,
			data : 'z??9LiveProtoےw?',
			game_short_name : 'jb5L1YFHdmzDhBRx',
		),
		$client->updateReadChannelOutbox(
			channel_id : -1579842363260331271,
			max_id : 81,
		),
		$client->updateDraftMessage(
			peer : $client->peerUser(
				user_id : 3536931575632633744,
			),
			top_msg_id : 85,
			saved_peer_id : $client->peerUser(
				user_id : -8822498876002723319,
			),
			draft : $client->draftMessageEmpty(
				date : 46,
			),
		),
		$client->updateReadFeaturedStickers(),
		$client->updateRecentStickers(),
		$client->updateConfig(),
		$client->updatePtsChanged(),
		$client->updateChannelWebPage(
			channel_id : -7637895643587419265,
			webpage : $client->webPageEmpty(
				id : -682700922868999600,
				url : 'https://docs.liveproto.dev',
			),
			pts : 55,
			pts_count : 50,
		),
		$client->updateDialogPinned(
			pinned : true,
			folder_id : 42,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
		),
		$client->updatePinnedDialogs(
			folder_id : 55,
			order : array(
				$client->dialogPeer(
					peer : $client->peerUser(...),
				),
				$client->dialogPeerFolder(
					folder_id : 42,
				),
			),
		),
		$client->updateBotWebhookJSON(
			data : $client->dataJSON(
				data : '8Yuv3o9pJVmeECIl',
			),
		),
		$client->updateBotWebhookJSONQuery(
			query_id : 5873675998004059544,
			data : $client->dataJSON(
				data : 'hbHdU7aqulY5iJy3',
			),
			timeout : 100,
		),
		$client->updateBotShippingQuery(
			query_id : -2608566595054225277,
			user_id : -8842298218263183982,
			payload : '>L?&?LiveProto?\\?B?',
			shipping_address : $client->postAddress(
				street_line1 : 'QxWKd18cRXnMrql9',
				street_line2 : 'PXsVcS2hxbKlJzj0',
				city : 'Uu3mM7JdzctCPNWG',
				state : '8QWEHqvfLeK6sI2r',
				country_iso2 : 'F5ukIcdo2T9GHSPz',
				post_code : 'uFCDEfATIjyHJxqe',
			),
		),
		$client->updateBotPrecheckoutQuery(
			query_id : 5442831717350329976,
			user_id : -8142765446213862170,
			payload : 'P?w??LiveProtoe屃|',
			info : $client->paymentRequestedInfo(
				name : 'QAqmztK1uwNlW4Rc',
				phone : '+1234567890',
				email : 'reply@liveproto.dev',
				shipping_address : $client->postAddress(...),
			),
			shipping_option_id : 'dfyWT1Ao67Sakijr',
			currency : 'Mwfq059aFjsC3EBk',
			total_amount : 4029616472647791662,
		),
		$client->updatePhoneCall(
			phone_call : $client->phoneCallEmpty(
				id : -3919082947243819881,
			),
		),
		$client->updateLangPackTooLong(
			lang_code : '1YncEKu4lxN9TW2U',
		),
		$client->updateLangPack(
			difference : $client->langPackDifference(
				lang_code : 'hItoXsfuwRicCSlb',
				from_version : 90,
				version : 81,
				strings : array(
					$client->langPackString(...),
					$client->langPackStringPluralized(...),
					$client->langPackStringDeleted(...),
				),
			),
		),
		$client->updateFavedStickers(),
		$client->updateChannelReadMessagesContents(
			channel_id : 7688485394345709214,
			top_msg_id : 54,
			saved_peer_id : $client->peerUser(
				user_id : -7364839093220601129,
			),
			messages : array(64),
		),
		$client->updateContactsReset(),
		$client->updateChannelAvailableMessages(
			channel_id : -5233531672879916130,
			available_min_id : 23,
		),
		$client->updateDialogUnreadMark(
			unread : true,
			peer : $client->dialogPeer(
				peer : $client->peerUser(...),
			),
			saved_peer_id : $client->peerUser(
				user_id : -6783783064108783653,
			),
		),
		$client->updateMessagePoll(
			poll_id : -3018364683214826585,
			poll : $client->poll(
				id : -2520136878747496174,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 57,
				close_date : 37,
			),
			results : $client->pollResults(
				min : true,
				results : array(
					$client->pollAnswerVoters(...),
				),
				total_voters : 81,
				recent_voters : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				solution : 'eAdIvg2O3aDSiulM',
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
				user_id : -2179656456995400396,
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
				until_date : 76,
			),
			version : 62,
		),
		$client->updateFolderPeers(
			folder_peers : array(
				$client->folderPeer(
					peer : $client->peerUser(...),
					folder_id : 10,
				),
			),
			pts : 45,
			pts_count : 17,
		),
		$client->updatePeerSettings(
			peer : $client->peerUser(
				user_id : -1711261436111644420,
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
				geo_distance : 24,
				request_chat_title : 'cXkJPrVsYjHMDTOz',
				request_chat_date : 24,
				business_bot_id : -4810833663911678538,
				business_bot_manage_url : 'https://docs.liveproto.dev',
				charge_paid_message_stars : 3745875111558493297,
				registration_month : '4wHxts12ESa0eZCv',
				phone_country : '+1234567890',
				name_change_date : 6,
				photo_change_date : 58,
			),
		),
		$client->updatePeerLocated(
			peers : array(
				$client->peerLocated(
					peer : $client->peerUser(...),
					expires : 49,
					distance : 55,
				),
				$client->peerSelfLocated(
					expires : 76,
				),
			),
		),
		$client->updateNewScheduledMessage(
			message : $client->messageEmpty(
				id : 18,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteScheduledMessages(
			peer : $client->peerUser(
				user_id : 3074666337356139950,
			),
			messages : array(52),
			sent_messages : array(67),
		),
		$client->updateTheme(
			theme : $client->theme(
				creator : true,
				default : true,
				for_chat : true,
				id : -8557516986938216607,
				access_hash : 807060161012096072,
				slug : 'UTVapZBgbNzJksSt',
				title : 'vOTckxVPR9GEwj5o',
				document : $client->documentEmpty(...),
				settings : array(
					$client->themeSettings(...),
				),
				emoticon : 'iW604HY8hBkJ9Qf2',
				installs_count : 13,
			),
		),
		$client->updateGeoLiveViewed(
			peer : $client->peerUser(
				user_id : -8696659912248999259,
			),
			msg_id : 67,
		),
		$client->updateLoginToken(),
		$client->updateMessagePollVote(
			poll_id : 4804931540142544629,
			peer : $client->peerUser(
				user_id : -7605836651060701590,
			),
			options : array('8?	?LiveProtoT??.?'),
			qts : 71,
		),
		$client->updateDialogFilter(
			id : 8,
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
				id : 18,
				title : $client->textWithEntities(...),
				emoticon : 'zyv8hfxVWImiJ7MC',
				color : 45,
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
			order : array(96),
		),
		$client->updateDialogFilters(),
		$client->updatePhoneCallSignalingData(
			phone_call_id : 1710965528321502246,
			data : 'KPB??LiveProtoN????',
		),
		$client->updateChannelMessageForwards(
			channel_id : -2039752386090662729,
			id : 94,
			forwards : 79,
		),
		$client->updateReadChannelDiscussionInbox(
			channel_id : 1210331770946621694,
			top_msg_id : 14,
			read_max_id : 89,
			broadcast_id : 1409205029792207662,
			broadcast_post : 97,
		),
		$client->updateReadChannelDiscussionOutbox(
			channel_id : 4615959297621199144,
			top_msg_id : 74,
			read_max_id : 32,
		),
		$client->updatePeerBlocked(
			blocked : true,
			blocked_my_stories_from : true,
			peer_id : $client->peerUser(
				user_id : -6505821982437933018,
			),
		),
		$client->updateChannelUserTyping(
			channel_id : -6126894679972376368,
			top_msg_id : 7,
			from_id : $client->peerUser(
				user_id : 3637094266189309091,
			),
			action : $client->sendMessageTypingAction(),
		),
		$client->updatePinnedMessages(
			pinned : true,
			peer : $client->peerUser(
				user_id : 5867893875643340379,
			),
			messages : array(9),
			pts : 64,
			pts_count : 44,
		),
		$client->updatePinnedChannelMessages(
			pinned : true,
			channel_id : -5544844578496746940,
			messages : array(66),
			pts : 58,
			pts_count : 59,
		),
		$client->updateChat(
			chat_id : 1792390507540328116,
		),
		$client->updateGroupCallParticipants(
			call : $client->inputGroupCall(
				id : -1600058414756193360,
				access_hash : -4799645889821794696,
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
					date : 80,
					active_date : 67,
					source : 51,
					volume : 27,
					about : 'Z8Ijqw0axygEefB5',
					raise_hand_rating : 3207914247523621950,
					video : $client->groupCallParticipantVideo(...),
					presentation : $client->groupCallParticipantVideo(...),
				),
			),
			version : 9,
		),
		$client->updateGroupCall(
			chat_id : 2839934917951939913,
			call : $client->groupCallDiscarded(
				id : -6008353708700754331,
				access_hash : 682735283289029998,
				duration : 54,
			),
		),
		$client->updatePeerHistoryTTL(
			peer : $client->peerUser(
				user_id : -2467506544460361820,
			),
			ttl_period : 73,
		),
		$client->updateChatParticipant(
			chat_id : 7497051153908155378,
			date : 3,
			actor_id : -7404377212486825669,
			user_id : 4826898748939640819,
			prev_participant : $client->chatParticipant(
				user_id : -1231534937803817649,
				inviter_id : 7532150830601145685,
				date : 80,
			),
			new_participant : $client->chatParticipant(
				user_id : 1391332922933432537,
				inviter_id : 6058991162091282343,
				date : 95,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'GbxAQiTCh8S5vsJX',
				admin_id : -2718176323758477534,
				date : 5,
				start_date : 68,
				expire_date : 1,
				usage_limit : 54,
				usage : 0,
				requested : 81,
				subscription_expired : 7,
				title : '4x2UWP1lv5G7Iq6p',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 82,
		),
		$client->updateChannelParticipant(
			via_chatlist : true,
			channel_id : 3950151431530497000,
			date : 53,
			actor_id : 6042408310394699126,
			user_id : 7711795968525137814,
			prev_participant : $client->channelParticipant(
				user_id : -5638436067762380764,
				date : 73,
				subscription_until_date : 21,
			),
			new_participant : $client->channelParticipant(
				user_id : 2616298780488476814,
				date : 74,
				subscription_until_date : 87,
			),
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'tiqGrQEmug0ARsjC',
				admin_id : 6394468874119145671,
				date : 22,
				start_date : 95,
				expire_date : 75,
				usage_limit : 55,
				usage : 27,
				requested : 41,
				subscription_expired : 79,
				title : 'XV42cxDvEhqzkpWi',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 62,
		),
		$client->updateBotStopped(
			user_id : 1218639535693187657,
			date : 79,
			stopped : $client->boolFalse(),
			qts : 34,
		),
		$client->updateGroupCallConnection(
			presentation : true,
			params : $client->dataJSON(
				data : 'Q9O0YpZe5VdtT6bD',
			),
		),
		$client->updateBotCommands(
			peer : $client->peerUser(
				user_id : 8691263933376994544,
			),
			bot_id : -1861576629832258584,
			commands : array(
				$client->botCommand(
					command : 'gFoVE0QhZbm1kNXU',
					description : 'T5PBve9bkMC8VcGS',
				),
			),
		),
		$client->updatePendingJoinRequests(
			peer : $client->peerUser(
				user_id : -9157661308427771941,
			),
			requests_pending : 10,
			recent_requesters : array(2188436208837101849),
		),
		$client->updateBotChatInviteRequester(
			peer : $client->peerUser(
				user_id : -7816465843140250583,
			),
			date : 93,
			user_id : 1531278980001895468,
			about : 'wgWsrut1DSaQbnNe',
			invite : $client->chatInviteExported(
				revoked : true,
				permanent : true,
				request_needed : true,
				link : 'rBw5CbMPVZ6kyWAq',
				admin_id : 2598160320210242791,
				date : 85,
				start_date : 66,
				expire_date : 49,
				usage_limit : 22,
				usage : 17,
				requested : 64,
				subscription_expired : 9,
				title : 'yUAq8GxHubkB5fQN',
				subscription_pricing : $client->starsSubscriptionPricing(...),
			),
			qts : 49,
		),
		$client->updateMessageReactions(
			peer : $client->peerUser(
				user_id : 8919886677422491754,
			),
			msg_id : 81,
			top_msg_id : 91,
			saved_peer_id : $client->peerUser(
				user_id : -2229010078029962780,
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
			query_id : -9140185182258360501,
		),
		$client->updateBotMenuButton(
			bot_id : -4357469114779525243,
			button : $client->botMenuButtonDefault(),
		),
		$client->updateSavedRingtones(),
		$client->updateTranscribedAudio(
			pending : true,
			peer : $client->peerUser(
				user_id : -486046388052791606,
			),
			msg_id : 91,
			transcription_id : 2669086985469580247,
			text : 'gj6Bkzu1CPxAhrbJ',
		),
		$client->updateReadFeaturedEmojiStickers(),
		$client->updateUserEmojiStatus(
			user_id : 1475384883859555529,
			emoji_status : $client->emojiStatusEmpty(),
		),
		$client->updateRecentEmojiStatuses(),
		$client->updateRecentReactions(),
		$client->updateMoveStickerSetToTop(
			masks : true,
			emojis : true,
			stickerset : -3349048466589206199,
		),
		$client->updateMessageExtendedMedia(
			peer : $client->peerUser(
				user_id : 753769931224666514,
			),
			msg_id : 84,
			extended_media : array(
				$client->messageExtendedMediaPreview(
					w : 22,
					h : 62,
					thumb : $client->photoSizeEmpty(...),
					video_duration : 79,
				),
				$client->messageExtendedMedia(
					media : $client->messageMediaEmpty(...),
				),
			),
		),
		$client->updateChannelPinnedTopic(
			pinned : true,
			channel_id : -3690849754611608772,
			topic_id : 77,
		),
		$client->updateChannelPinnedTopics(
			channel_id : 4339364240979146581,
			order : array(65),
		),
		$client->updateUser(
			user_id : 4883937962344019428,
		),
		$client->updateAutoSaveSettings(),
		$client->updateStory(
			peer : $client->peerUser(
				user_id : 6797848141708361912,
			),
			story : $client->storyItemDeleted(
				id : 66,
			),
		),
		$client->updateReadStories(
			peer : $client->peerUser(
				user_id : 4768895598012018050,
			),
			max_id : 70,
		),
		$client->updateStoryID(
			id : 85,
			random_id : 7581262306231542205,
		),
		$client->updateStoriesStealthMode(
			stealth_mode : $client->storiesStealthMode(
				active_until_date : 79,
				cooldown_until_date : 19,
			),
		),
		$client->updateSentStoryReaction(
			peer : $client->peerUser(
				user_id : 725416966318517500,
			),
			story_id : 16,
			reaction : $client->reactionEmpty(),
		),
		$client->updateBotChatBoost(
			peer : $client->peerUser(
				user_id : 1005360009854957859,
			),
			boost : $client->boost(
				gift : true,
				giveaway : true,
				unclaimed : true,
				id : 'DmCMbqguJozt9580',
				user_id : -4572411523259559765,
				giveaway_msg_id : 47,
				date : 9,
				expires : 25,
				used_gift_slug : 'XrGvKnh9D1NtjSVk',
				multiplier : 94,
				stars : -4172310762101004658,
			),
			qts : 7,
		),
		$client->updateChannelViewForumAsMessages(
			channel_id : 4114193766638767195,
			enabled : $client->boolFalse(),
		),
		$client->updatePeerWallpaper(
			wallpaper_overridden : true,
			peer : $client->peerUser(
				user_id : -1817662306769760399,
			),
			wallpaper : $client->wallPaper(
				id : 1329442925172289465,
				creator : true,
				default : true,
				pattern : true,
				dark : true,
				access_hash : 7181194962700935726,
				slug : '2XB8sxR3AQ5lJq7I',
				document : $client->documentEmpty(...),
				settings : $client->wallPaperSettings(...),
			),
		),
		$client->updateBotMessageReaction(
			peer : $client->peerUser(
				user_id : 7773412083282717053,
			),
			msg_id : 76,
			date : 96,
			actor : $client->peerUser(
				user_id : -3533640584588676406,
			),
			old_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'AZOyMUGnVDt6PWHT',
				),
				$client->reactionCustomEmoji(
					document_id : 3284104578469722313,
				),
				$client->reactionPaid(),
			),
			new_reactions : array(
				$client->reactionEmpty(),
				$client->reactionEmoji(
					emoticon : 'xbLBGqU8QdCST2uF',
				),
				$client->reactionCustomEmoji(
					document_id : -6709924098882494504,
				),
				$client->reactionPaid(),
			),
			qts : 46,
		),
		$client->updateBotMessageReactions(
			peer : $client->peerUser(
				user_id : -7473289927794454307,
			),
			msg_id : 31,
			date : 37,
			reactions : array(
				$client->reactionCount(
					chosen_order : 23,
					reaction : $client->reactionEmpty(...),
					count : 84,
				),
			),
			qts : 61,
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
					folder_id : 21,
				),
			),
		),
		$client->updateSavedReactionTags(),
		$client->updateSmsJob(
			job_id : 'L1JZ2A6C9T4yzIXG',
		),
		$client->updateQuickReplies(
			quick_replies : array(
				$client->quickReply(
					shortcut_id : 35,
					shortcut : 'AGkJ4BSx9cpXjZyl',
					top_message : 6,
					count : 30,
				),
			),
		),
		$client->updateNewQuickReply(
			quick_reply : $client->quickReply(
				shortcut_id : 42,
				shortcut : 'wajW5XVLR8Qexzlm',
				top_message : 58,
				count : 92,
			),
		),
		$client->updateDeleteQuickReply(
			shortcut_id : 84,
		),
		$client->updateQuickReplyMessage(
			message : $client->messageEmpty(
				id : 55,
				peer_id : $client->peerUser(...),
			),
		),
		$client->updateDeleteQuickReplyMessages(
			shortcut_id : 22,
			messages : array(3),
		),
		$client->updateBotBusinessConnect(
			connection : $client->botBusinessConnection(
				disabled : true,
				connection_id : 'PT3NU89K0BH74cmi',
				user_id : -3693568457462405074,
				dc_id : 41,
				date : 16,
				rights : $client->businessBotRights(...),
			),
			qts : 60,
		),
		$client->updateBotNewBusinessMessage(
			connection_id : 'yVEwOx52UvF1qpAH',
			message : $client->messageEmpty(
				id : 49,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 92,
				peer_id : $client->peerUser(...),
			),
			qts : 24,
		),
		$client->updateBotEditBusinessMessage(
			connection_id : 'tJz9BHIvFN4yxkjg',
			message : $client->messageEmpty(
				id : 12,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 0,
				peer_id : $client->peerUser(...),
			),
			qts : 39,
		),
		$client->updateBotDeleteBusinessMessage(
			connection_id : 'z5mqSCyJjUfbIRDP',
			peer : $client->peerUser(
				user_id : -4637893835778390681,
			),
			messages : array(7),
			qts : 89,
		),
		$client->updateNewStoryReaction(
			story_id : 57,
			peer : $client->peerUser(
				user_id : 8082378331770535272,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->updateStarsBalance(
			balance : $client->starsAmount(
				amount : -2379125993694168770,
				nanos : 51,
			),
		),
		$client->updateBusinessBotCallbackQuery(
			query_id : 4806287660887369644,
			user_id : 6128123173779032947,
			connection_id : 'umZ2DEULF5oRAyjJ',
			message : $client->messageEmpty(
				id : 81,
				peer_id : $client->peerUser(...),
			),
			reply_to_message : $client->messageEmpty(
				id : 44,
				peer_id : $client->peerUser(...),
			),
			chat_instance : -7568528886190763159,
			data : '???LiveProto??ǐ',
		),
		$client->updateStarsRevenueStatus(
			peer : $client->peerUser(
				user_id : 351049001904999634,
			),
			status : $client->starsRevenueStatus(
				withdrawal_enabled : true,
				current_balance : $client->starsAmount(...),
				available_balance : $client->starsAmount(...),
				overall_revenue : $client->starsAmount(...),
				next_withdrawal_at : 91,
			),
		),
		$client->updateBotPurchasedPaidMedia(
			user_id : -8962040005486598476,
			payload : 'R53vw20T9npeJZWN',
			qts : 90,
		),
		$client->updatePaidReactionPrivacy(
			private : $client->paidReactionPrivacyDefault(),
		),
		$client->updateSentPhoneCode(
			sent_code : $client->auth->sentCode(
				type : $client->auth->sentCodeTypeApp(...),
				phone_code_hash : '+1234567890',
				next_type : $client->auth->codeTypeSms(...),
				timeout : 89,
			),
		),
		$client->updateGroupCallChainBlocks(
			call : $client->inputGroupCall(
				id : 4508289664974453740,
				access_hash : -7707952514970689695,
			),
			sub_chain_id : 12,
			blocks : array('??LiveProto?G??P'),
			next_offset : 61,
		),
		$client->updateReadMonoForumInbox(
			channel_id : -3854765393796050268,
			saved_peer_id : $client->peerUser(
				user_id : -2090822691876655787,
			),
			read_max_id : 42,
		),
		$client->updateReadMonoForumOutbox(
			channel_id : -7244525376729918165,
			saved_peer_id : $client->peerUser(
				user_id : 2222105239668618040,
			),
			read_max_id : 13,
		),
		$client->updateMonoForumNoPaidException(
			exception : true,
			channel_id : 2037526766982196639,
			saved_peer_id : $client->peerUser(
				user_id : 2986886034883955956,
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -5307367201230798179,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -9058562044608652098,
			title : 'pw1RJmgaANXG6bZq',
			photo : $client->chatPhotoEmpty(),
			participants_count : 96,
			date : 51,
			version : 0,
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
				until_date : 94,
			),
		),
		$client->chatForbidden(
			id : 5740208106968820509,
			title : 'rRWau0XMiUjGNS65',
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
			id : 4349138404388783866,
			access_hash : 7583690645636455718,
			title : 'UH6mAGds87uworTa',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 95,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'bVq0tomag8M2fGYL',
					reason : 'obJpe0N1jin4cGQ9',
					text : '0IKLk2rESnoXue7D',
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
				until_date : 24,
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
				until_date : 87,
			),
			participants_count : 42,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 3,
			color : $client->peerColor(
				color : 35,
				background_emoji_id : 702304703091362655,
			),
			profile_color : $client->peerColor(
				color : 29,
				background_emoji_id : -2337776782172196650,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 19,
			subscription_until_date : 79,
			bot_verification_icon : 6861264987214269748,
			send_paid_messages_stars : 5448267885017241599,
			linked_monoforum_id : 6109413742186568621,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -3449325237547154606,
			access_hash : -4478077523435961252,
			title : 'tcg9Ua47ZwLvHrKX',
			until_date : 14,
		),
	),
	users : array(
		$client->userEmpty(
			id : -6891408638157086193,
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
			id : -1046447669717020433,
			access_hash : -3646686200751751015,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 28,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'O9x7wvHlsCYmRMJr',
					reason : 'U3kGLqZstbh69wAD',
					text : 'sXZTn7D3PS10UiLz',
				),
			),
			bot_inline_placeholder : '3yH0arMXjsodTnf1',
			lang_code : 'dr9DFiCxzsvof3jH',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 100,
			color : $client->peerColor(
				color : 20,
				background_emoji_id : -5722043320139382139,
			),
			profile_color : $client->peerColor(
				color : 80,
				background_emoji_id : -2570937435922618618,
			),
			bot_active_users : 85,
			bot_verification_icon : -6680744451354095098,
			send_paid_messages_stars : 115873690164538370,
		),
	),
);
```