# message

**Description** : *A message*

**Layer** : 211

```tl
message#9815cec8 flags:# out:flags.1?true mentioned:flags.4?true media_unread:flags.5?true silent:flags.13?true post:flags.14?true from_scheduled:flags.18?true legacy:flags.19?true edit_hide:flags.21?true pinned:flags.24?true noforwards:flags.26?true invert_media:flags.27?true flags2:# offline:flags2.1?true video_processing_pending:flags2.4?true paid_suggested_post_stars:flags2.8?true paid_suggested_post_ton:flags2.9?true id:int from_id:flags.8?Peer from_boosts_applied:flags.29?int peer_id:Peer saved_peer_id:flags.28?Peer fwd_from:flags.2?MessageFwdHeader via_bot_id:flags.11?long via_business_bot_id:flags2.0?long reply_to:flags.3?MessageReplyHeader date:int message:string media:flags.9?MessageMedia reply_markup:flags.6?ReplyMarkup entities:flags.7?Vector<MessageEntity> views:flags.10?int forwards:flags.10?int replies:flags.23?MessageReplies edit_date:flags.15?int post_author:flags.16?string grouped_id:flags.17?long reactions:flags.20?MessageReactions restriction_reason:flags.22?Vector<RestrictionReason> ttl_period:flags.25?int quick_reply_shortcut_id:flags.30?int effect:flags2.2?long factcheck:flags2.3?FactCheck report_delivery_until_date:flags2.5?int paid_message_stars:flags2.6?long suggested_post:flags2.7?SuggestedPost = Message;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **out** | [`flags.1?true`](type/true) | Is this an outgoing message |
| **mentioned** | [`flags.4?true`](type/true) | Whether we were mentioned in this message |
| **media_unread** | [`flags.5?true`](type/true) | Whether there are unread media attachments in this message |
| **silent** | [`flags.13?true`](type/true) | Whether this is a silent message (no notification triggered) |
| **post** | [`flags.14?true`](type/true) | Whether this is a channel post |
| **from_scheduled** | [`flags.18?true`](type/true) | Whether this is a scheduled message |
| **legacy** | [`flags.19?true`](type/true) | This is a legacy message: it has to be refetched with the new layer |
| **edit_hide** | [`flags.21?true`](type/true) | Whether the message should be shown as not modified to the user, even if an edit date is present |
| **pinned** | [`flags.24?true`](type/true) | Whether this message is pinned |
| **noforwards** | [`flags.26?true`](type/true) | Whether this message is protected and thus cannot be forwarded; clients should also prevent users from saving attached media (i.e. videos should only be streamed, photos should be kept in RAM, et cetera) |
| **invert_media** | [`flags.27?true`](type/true) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom |
| <mark>flags2</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **offline** | [`flags2.1?true`](type/true) | If set, the message was sent because of a scheduled action by the message sender, for example, as away, or a greeting service message |
| **video_processing_pending** | [`flags2.4?true`](type/true) | The video contained in the message is currently being processed by the server (i.e. to generate alternative qualities, that will be contained in the final messageMediaDocument.alt_document), and will be sent once the video is processed, which will happen approximately at the specified date (i.e. messages with this flag set should be treated similarly to scheduled messages, but instead of the scheduled date, date contains the estimated conversion date). See here » for more info |
| **paid_suggested_post_stars** | [`flags2.8?true`](type/true) | NOTHING |
| **paid_suggested_post_ton** | [`flags2.9?true`](type/true) | NOTHING |
| <mark>id</mark> | [`int`](type/int) | ID of the message |
| **from_id** | [`flags.8?Peer`](type/Peer) | ID of the sender of the message |
| **from_boosts_applied** | [`flags.29?int`](type/int) | Supergroups only, contains the number of boosts this user has given the current supergroup, and should be shown in the UI in the header of the message. Only present for incoming messages from non-anonymous supergroup members that have boosted the supergroup. Note that this counter should be locally overridden for non-anonymous outgoing messages, according to the current value of channelFull.boosts_applied, to ensure the value is correct even for messages sent by the current user before a supergroup was boosted (or after a boost has expired or the number of boosts has changed); do not update this value for incoming messages from other users, even if their boosts have changed |
| <mark>peer_id</mark> | [`Peer`](type/Peer) | Peer ID, the chat where this message was sent |
| **saved_peer_id** | [`flags.28?Peer`](type/Peer) | Messages fetched from a saved messages dialog » will have peer=inputPeerSelf and the saved_peer_id flag set to the ID of the saved dialog |
| **fwd_from** | [`flags.2?MessageFwdHeader`](type/MessageFwdHeader) | Info about forwarded messages |
| **via_bot_id** | [`flags.11?long`](type/long) | ID of the inline bot that generated the message |
| **via_business_bot_id** | [`flags2.0?long`](type/long) | Whether the message was sent by the business bot specified in via_bot_id on behalf of the user |
| **reply_to** | [`flags.3?MessageReplyHeader`](type/MessageReplyHeader) | Reply information |
| <mark>date</mark> | [`int`](type/int) | Date of the message |
| <mark>message</mark> | [`string`](type/string) | The message |
| **media** | [`flags.9?MessageMedia`](type/MessageMedia) | Media attachment |
| **reply_markup** | [`flags.6?ReplyMarkup`](type/ReplyMarkup) | Reply markup (bot/inline keyboards) |
| **entities** | [`flags.7?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| **views** | [`flags.10?int`](type/int) | View count for channel posts |
| **forwards** | [`flags.10?int`](type/int) | Forward counter |
| **replies** | [`flags.23?MessageReplies`](type/MessageReplies) | Info about post comments (for channels) or message replies (for groups) |
| **edit_date** | [`flags.15?int`](type/int) | Last edit date of this message |
| **post_author** | [`flags.16?string`](type/string) | Name of the author of this message for channel posts (with signatures enabled) |
| **grouped_id** | [`flags.17?long`](type/long) | Multiple media messages sent using messages.sendMultiMedia with the same grouped ID indicate an album or media group |
| **reactions** | [`flags.20?MessageReactions`](type/MessageReactions) | Reactions to this message |
| **restriction_reason** | [`flags.22?Vector<RestrictionReason>`](type/RestrictionReason) | Contains the reason why access to this message must be restricted |
| **ttl_period** | [`flags.25?int`](type/int) | Time To Live of the message, once message.date+message.ttl_period === time(), the message will be deleted on the server, and must be deleted locally as well |
| **quick_reply_shortcut_id** | [`flags.30?int`](type/int) | If set, this message is a quick reply shortcut message » (note that quick reply shortcut messages sent to a private chat will not have this field set) |
| **effect** | [`flags2.2?long`](type/long) | A message effect that should be played as specified here » |
| **factcheck** | [`flags2.3?FactCheck`](type/FactCheck) | Represents a fact-check » |
| **report_delivery_until_date** | [`flags2.5?int`](type/int) | NOTHING |
| **paid_message_stars** | [`flags2.6?long`](type/long) | NOTHING |
| **suggested_post** | [`flags2.7?SuggestedPost`](type/SuggestedPost) | NOTHING |

---

## Type

[Message](type/Message)

---

## Example

```php
$message = $client->message(
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
	id : 39,
	from_id : $client->peerUser(
		user_id : -5510436105395036202,
	),
	from_boosts_applied : 52,
	peer_id : $client->peerUser(
		user_id : 5298442549662725321,
	),
	saved_peer_id : $client->peerUser(
		user_id : 4452453466628458566,
	),
	fwd_from : $client->messageFwdHeader(
		imported : true,
		saved_out : true,
		from_id : $client->peerUser(
			user_id : 4968494117798088806,
		),
		from_name : 'uTfgwjpoYKUJAyr2',
		date : 22,
		channel_post : 30,
		post_author : 'KcNkUPQ1qbT6Ihsw',
		saved_from_peer : $client->peerUser(
			user_id : 6847101042717449363,
		),
		saved_from_msg_id : 22,
		saved_from_id : $client->peerUser(
			user_id : 8390707712744993552,
		),
		saved_from_name : 'RVpKS7wlBv4WD8tF',
		saved_date : 0,
		psa_type : 'T3lwoW1Ss8rpQzU7',
	),
	via_bot_id : 2453557144719811750,
	via_business_bot_id : -8219649993831770757,
	reply_to : $client->messageReplyHeader(
		reply_to_scheduled : true,
		forum_topic : true,
		quote : true,
		reply_to_msg_id : 66,
		reply_to_peer_id : $client->peerUser(
			user_id : -4531275560131946435,
		),
		reply_from : $client->messageFwdHeader(
			imported : true,
			saved_out : true,
			from_id : $client->peerUser(...),
			from_name : 'KRQuqA4k0512XUyY',
			date : 35,
			channel_post : 84,
			post_author : 'DXZGuRqEl7B0tbKT',
			saved_from_peer : $client->peerUser(...),
			saved_from_msg_id : 14,
			saved_from_id : $client->peerUser(...),
			saved_from_name : 'Pq7YHJusNB9bk2CD',
			saved_date : 9,
			psa_type : 'W1JqtREyaFMIbuVA',
		),
		reply_media : $client->messageMediaEmpty(),
		reply_to_top_id : 89,
		quote_text : 'YMpWsaLDVi8d4bz2',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 4,
				length : 35,
			),
			$client->messageEntityMention(
				offset : 88,
				length : 70,
			),
			$client->messageEntityHashtag(
				offset : 71,
				length : 16,
			),
			$client->messageEntityBotCommand(
				offset : 65,
				length : 99,
			),
			$client->messageEntityUrl(
				offset : 93,
				length : 3,
			),
			$client->messageEntityEmail(
				offset : 44,
				length : 90,
			),
			$client->messageEntityBold(
				offset : 95,
				length : 85,
			),
			$client->messageEntityItalic(
				offset : 28,
				length : 15,
			),
			$client->messageEntityCode(
				offset : 34,
				length : 60,
			),
			$client->messageEntityPre(
				offset : 31,
				length : 2,
				language : 'WJpiOHCK0bfFRLku',
			),
			$client->messageEntityTextUrl(
				offset : 18,
				length : 23,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 29,
				length : 84,
				user_id : -3347285416250754404,
			),
			$client->inputMessageEntityMentionName(
				offset : 99,
				length : 34,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 89,
				length : 6,
			),
			$client->messageEntityCashtag(
				offset : 44,
				length : 15,
			),
			$client->messageEntityUnderline(
				offset : 20,
				length : 56,
			),
			$client->messageEntityStrike(
				offset : 29,
				length : 77,
			),
			$client->messageEntityBankCard(
				offset : 84,
				length : 16,
			),
			$client->messageEntitySpoiler(
				offset : 29,
				length : 78,
			),
			$client->messageEntityCustomEmoji(
				offset : 51,
				length : 0,
				document_id : -3619452448781948936,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 84,
				length : 67,
			),
		),
		quote_offset : 100,
		todo_item_id : 20,
	),
	date : 6,
	message : 'JyN498RXDxnLFicC',
	media : $client->messageMediaEmpty(),
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
	entities : array(
		$client->messageEntityUnknown(
			offset : 64,
			length : 20,
		),
		$client->messageEntityMention(
			offset : 51,
			length : 35,
		),
		$client->messageEntityHashtag(
			offset : 3,
			length : 6,
		),
		$client->messageEntityBotCommand(
			offset : 24,
			length : 71,
		),
		$client->messageEntityUrl(
			offset : 32,
			length : 26,
		),
		$client->messageEntityEmail(
			offset : 5,
			length : 46,
		),
		$client->messageEntityBold(
			offset : 35,
			length : 13,
		),
		$client->messageEntityItalic(
			offset : 42,
			length : 63,
		),
		$client->messageEntityCode(
			offset : 96,
			length : 4,
		),
		$client->messageEntityPre(
			offset : 92,
			length : 44,
			language : 'ClNpIzrhTRijaXcA',
		),
		$client->messageEntityTextUrl(
			offset : 11,
			length : 23,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 6,
			length : 45,
			user_id : -5566715995845273117,
		),
		$client->inputMessageEntityMentionName(
			offset : 78,
			length : 64,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 48,
			length : 87,
		),
		$client->messageEntityCashtag(
			offset : 67,
			length : 67,
		),
		$client->messageEntityUnderline(
			offset : 18,
			length : 5,
		),
		$client->messageEntityStrike(
			offset : 5,
			length : 0,
		),
		$client->messageEntityBankCard(
			offset : 57,
			length : 26,
		),
		$client->messageEntitySpoiler(
			offset : 63,
			length : 12,
		),
		$client->messageEntityCustomEmoji(
			offset : 77,
			length : 99,
			document_id : 7504457340214246973,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 73,
			length : 22,
		),
	),
	views : 81,
	forwards : 37,
	replies : $client->messageReplies(
		comments : true,
		replies : 39,
		replies_pts : 41,
		recent_repliers : array(
			$client->peerUser(
				user_id : 6810616325850352761,
			),
			$client->peerChat(
				chat_id : -3889408606280148282,
			),
			$client->peerChannel(
				channel_id : -582701217878442246,
			),
		),
		channel_id : 299570860656222367,
		max_id : 50,
		read_max_id : 86,
	),
	edit_date : 82,
	post_author : '1EbOzPq5h8KCuNjp',
	grouped_id : -2415494825128035002,
	reactions : $client->messageReactions(
		min : true,
		can_see_list : true,
		reactions_as_tags : true,
		results : array(
			$client->reactionCount(
				chosen_order : 73,
				reaction : $client->reactionEmpty(...),
				count : 34,
			),
		),
		recent_reactions : array(
			$client->messagePeerReaction(
				big : true,
				unread : true,
				my : true,
				peer_id : $client->peerUser(...),
				date : 64,
				reaction : $client->reactionEmpty(...),
			),
		),
		top_reactors : array(
			$client->messageReactor(
				top : true,
				my : true,
				anonymous : true,
				peer_id : $client->peerUser(...),
				count : 83,
			),
		),
	),
	restriction_reason : array(
		$client->restrictionReason(
			platform : 'hmeR8Q50IpM7bUqN',
			reason : '7rQmHMgEDoUqtOb4',
			text : 'dRm0eY4UkrgHhPFD',
		),
	),
	ttl_period : 97,
	quick_reply_shortcut_id : 63,
	effect : 2473833096424855368,
	factcheck : $client->factCheck(
		need_check : true,
		country : 'z2D4b0ANk7RfgQsj',
		text : $client->textWithEntities(
			text : 'GJduED543A1RwVqi',
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
		hash : 565873959102168368,
	),
	report_delivery_until_date : 93,
	paid_message_stars : -8108845177128258389,
	suggested_post : $client->suggestedPost(
		accepted : true,
		rejected : true,
		price : $client->starsAmount(
			amount : 1754784982001095379,
			nanos : 72,
		),
		schedule_date : 1,
	),
);
```