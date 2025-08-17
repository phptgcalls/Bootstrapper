# starsTransaction

**Description** : *Represents a Telegram Stars transaction »*

**Layer** : 211

```tl
starsTransaction#13659eb0 flags:# refund:flags.3?true pending:flags.4?true failed:flags.6?true gift:flags.10?true reaction:flags.11?true stargift_upgrade:flags.18?true business_transfer:flags.21?true stargift_resale:flags.22?true posts_search:flags.24?true id:string amount:StarsAmount date:int peer:StarsTransactionPeer title:flags.0?string description:flags.1?string photo:flags.2?WebDocument transaction_date:flags.5?int transaction_url:flags.5?string bot_payload:flags.7?bytes msg_id:flags.8?int extended_media:flags.9?Vector<MessageMedia> subscription_period:flags.12?int giveaway_post_id:flags.13?int stargift:flags.14?StarGift floodskip_number:flags.15?int starref_commission_permille:flags.16?int starref_peer:flags.17?Peer starref_amount:flags.17?StarsAmount paid_messages:flags.19?int premium_gift_months:flags.20?int ads_proceeds_from_date:flags.23?int ads_proceeds_to_date:flags.23?int = StarsTransaction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **refund** | [`flags.3?true`](type/true) | Whether this transaction is a refund |
| **pending** | [`flags.4?true`](type/true) | The transaction is currently pending |
| **failed** | [`flags.6?true`](type/true) | This transaction has failed |
| **gift** | [`flags.10?true`](type/true) | This transaction was a gift from the user in peer.peer |
| **reaction** | [`flags.11?true`](type/true) | This transaction is a paid reaction » |
| **stargift_upgrade** | [`flags.18?true`](type/true) | NOTHING |
| **business_transfer** | [`flags.21?true`](type/true) | NOTHING |
| **stargift_resale** | [`flags.22?true`](type/true) | NOTHING |
| **posts_search** | [`flags.24?true`](type/true) | NOTHING |
| <mark>id</mark> | [`string`](type/string) | Transaction ID |
| <mark>amount</mark> | [`StarsAmount`](type/StarsAmount) | NOTHING |
| <mark>date</mark> | [`int`](type/int) | Date of the transaction (unixtime) |
| <mark>peer</mark> | [`StarsTransactionPeer`](type/StarsTransactionPeer) | Source of the incoming transaction, or its recipient for outgoing transactions |
| **title** | [`flags.0?string`](type/string) | For transactions with bots, title of the bought product |
| **description** | [`flags.1?string`](type/string) | For transactions with bots, description of the bought product |
| **photo** | [`flags.2?WebDocument`](type/WebDocument) | For transactions with bots, photo of the bought product |
| **transaction_date** | [`flags.5?int`](type/int) | If neither pending nor failed are set, the transaction was completed successfully, and this field will contain the point in time (Unix timestamp) when the withdrawal was completed successfully |
| **transaction_url** | [`flags.5?string`](type/string) | If neither pending nor failed are set, the transaction was completed successfully, and this field will contain a URL where the withdrawal transaction can be viewed |
| **bot_payload** | [`flags.7?bytes`](type/bytes) | Bot specified invoice payload (i.e. the payload passed to inputMediaInvoice when creating the invoice) |
| **msg_id** | [`flags.8?int`](type/int) | For paid media transactions », message ID of the paid media posted to peer.peer (can point to a deleted message; either way, extended_media will always contain the bought media) |
| **extended_media** | [`flags.9?Vector<MessageMedia>`](type/MessageMedia) | The purchased paid media » |
| **subscription_period** | [`flags.12?int`](type/int) | The number of seconds between consecutive Telegram Star debiting for Telegram Star subscriptions » |
| **giveaway_post_id** | [`flags.13?int`](type/int) | ID of the message containing the messageMediaGiveaway, for incoming star giveaway prizes |
| **stargift** | [`flags.14?StarGift`](type/StarGift) | This transaction indicates a purchase or a sale (conversion back to Stars) of a gift » |
| **floodskip_number** | [`flags.15?int`](type/int) | This transaction is payment for paid bot broadcasts.  Paid broadcasts are only allowed if the allow_paid_floodskip parameter of messages.sendMessage and other message sending methods is set while trying to broadcast more than 30 messages per second to bot users. The integer value returned by this flag indicates the number of billed API calls |
| **starref_commission_permille** | [`flags.16?int`](type/int) | This transaction is the receival (or refund) of an affiliate commission (i.e. this is the transaction received by the peer that created the referral link, flag 17 is for transactions made by users that imported the referral link) |
| **starref_peer** | [`flags.17?Peer`](type/Peer) | For transactions made by referred users, the peer that received the affiliate commission |
| **starref_amount** | [`flags.17?StarsAmount`](type/StarsAmount) | For transactions made by referred users, the amount of Telegram Stars received by the affiliate, can be negative for refunds |
| **paid_messages** | [`flags.19?int`](type/int) | NOTHING |
| **premium_gift_months** | [`flags.20?int`](type/int) | NOTHING |
| **ads_proceeds_from_date** | [`flags.23?int`](type/int) | NOTHING |
| **ads_proceeds_to_date** | [`flags.23?int`](type/int) | NOTHING |

---

## Type

[StarsTransaction](type/StarsTransaction)

---

## Example

```php
$starsTransaction = $client->starsTransaction(
	refund : true,
	pending : true,
	failed : true,
	gift : true,
	reaction : true,
	stargift_upgrade : true,
	business_transfer : true,
	stargift_resale : true,
	posts_search : true,
	id : 'CV2q9Zk5jf7iuODL',
	amount : $client->starsAmount(
		amount : -135181461779178448,
		nanos : 75,
	),
	date : 91,
	peer : $client->starsTransactionPeerUnsupported(),
	title : 'b9NIo1Dnp2QSgrLl',
	description : 'TGU2IR1xPfNdiCV0',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -5114272601623947225,
		size : 1,
		mime_type : 'Aptr8NS17oj3qGIL',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 87,
				h : 13,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'zbUtByCk1VLve7FI',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : 1858481.345703125,
				w : 84,
				h : 89,
				preload_prefix_size : 4,
				video_start_ts : 651525.517578125,
				video_codec : '7iyU13vF0QzIR9na',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 0,
				title : '4Yu7GqinyrhBLmA5',
				performer : 'iwqKC4GevRVDynPM',
				waveform : 'l?A<
LiveProto?՜*?',
			),
			$client->documentAttributeFilename(
				file_name : 'UJRsehvbB1aYMEp8',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'wPzkqrjVoCaULfIQ',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	transaction_date : 27,
	transaction_url : 'https://docs.liveproto.dev',
	bot_payload : '??ivLiveProto<q?W',
	msg_id : 62,
	extended_media : array(
		$client->messageMediaEmpty(),
		$client->messageMediaPhoto(
			spoiler : true,
			photo : $client->photoEmpty(
				id : -3640272014473925443,
			),
			ttl_seconds : 81,
		),
		$client->messageMediaGeo(
			geo : $client->geoPointEmpty(),
		),
		$client->messageMediaContact(
			phone_number : '+1234567890',
			first_name : 'Tak',
			last_name : 'None',
			vcard : 'sbXRtpDTMgS1ne79',
			user_id : -8233244098040155682,
		),
		$client->messageMediaUnsupported(),
		$client->messageMediaDocument(
			nopremium : true,
			spoiler : true,
			video : true,
			round : true,
			voice : true,
			document : $client->documentEmpty(
				id : -979294826197951480,
			),
			alt_documents : array(
				$client->documentEmpty(
					id : -4256504795681456483,
				),
				$client->document(
					id : -2150917736475825743,
					access_hash : 1980131908571407037,
					file_reference : '2c???LiveProto?9??',
					date : 0,
					mime_type : 'LBharzM3pTOvidJU',
					size : 3075021415975646410,
					thumbs : array(
						$client->photoSizeEmpty(...),
						$client->photoSize(...),
						$client->photoCachedSize(...),
						$client->photoStrippedSize(...),
						$client->photoSizeProgressive(...),
						$client->photoPathSize(...),
					),
					video_thumbs : array(
						$client->videoSize(...),
						$client->videoSizeEmojiMarkup(...),
						$client->videoSizeStickerMarkup(...),
					),
					dc_id : 34,
					attributes : array(
						$client->documentAttributeImageSize(...),
						$client->documentAttributeAnimated(...),
						$client->documentAttributeSticker(...),
						$client->documentAttributeVideo(...),
						$client->documentAttributeAudio(...),
						$client->documentAttributeFilename(...),
						$client->documentAttributeHasStickers(...),
						$client->documentAttributeCustomEmoji(...),
					),
				),
			),
			video_cover : $client->photoEmpty(
				id : 6093001057490137174,
			),
			video_timestamp : 57,
			ttl_seconds : 21,
		),
		$client->messageMediaWebPage(
			force_large_media : true,
			force_small_media : true,
			manual : true,
			safe : true,
			webpage : $client->webPageEmpty(
				id : -731322028196662876,
				url : 'https://docs.liveproto.dev',
			),
		),
		$client->messageMediaVenue(
			geo : $client->geoPointEmpty(),
			title : '09wFWXKVE6vxyz4D',
			address : 'K9UvH14c7lOYqxiu',
			provider : 'DoWzGfBK3twc05qP',
			venue_id : 'IOyXUgmBfSZL7wod',
			venue_type : 'xhM2F6H4gfUzoeYJ',
		),
		$client->messageMediaGame(
			game : $client->game(
				id : -8406141732005972953,
				access_hash : 663341714788662939,
				short_name : 'eLnFicxYO1WDZRot',
				title : 'N2QXvcrFe3xGCjLi',
				description : 'mTVIZ9b18ui5zJHp',
				photo : $client->photoEmpty(...),
				document : $client->documentEmpty(...),
			),
		),
		$client->messageMediaInvoice(
			shipping_address_requested : true,
			test : true,
			title : 'SbiPBMYxlCfngaQ3',
			description : '4AfgxUT5eaOV6QmL',
			photo : $client->webDocument(
				url : 'https://docs.liveproto.dev',
				access_hash : 6318677468309776527,
				size : 60,
				mime_type : 'j9PLKdGnaUsRvpgD',
				attributes : array(
					$client->documentAttributeImageSize(...),
					$client->documentAttributeAnimated(...),
					$client->documentAttributeSticker(...),
					$client->documentAttributeVideo(...),
					$client->documentAttributeAudio(...),
					$client->documentAttributeFilename(...),
					$client->documentAttributeHasStickers(...),
					$client->documentAttributeCustomEmoji(...),
				),
			),
			receipt_msg_id : 92,
			currency : 'JSzACGTfeB35Drds',
			total_amount : 411658741613915719,
			start_param : 'NAfS3DlBK6m7uciw',
			extended_media : $client->messageExtendedMediaPreview(
				w : 15,
				h : 38,
				thumb : $client->photoSizeEmpty(...),
				video_duration : 56,
			),
		),
		$client->messageMediaGeoLive(
			geo : $client->geoPointEmpty(),
			heading : 6,
			period : 69,
			proximity_notification_radius : 55,
		),
		$client->messageMediaPoll(
			poll : $client->poll(
				id : -3877181796613184517,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 19,
				close_date : 90,
			),
			results : $client->pollResults(
				min : true,
				results : array(
					$client->pollAnswerVoters(...),
				),
				total_voters : 84,
				recent_voters : array(
					$client->peerUser(...),
					$client->peerChat(...),
					$client->peerChannel(...),
				),
				solution : 'ft0paykCZwrhR6sF',
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
		$client->messageMediaDice(
			value : 28,
			emoticon : 't0vG9AVO1kKEfjCm',
		),
		$client->messageMediaStory(
			via_mention : true,
			peer : $client->peerUser(
				user_id : -6100934873410040677,
			),
			id : 29,
			story : $client->storyItemDeleted(
				id : 33,
			),
		),
		$client->messageMediaGiveaway(
			only_new_subscribers : true,
			winners_are_visible : true,
			channels : array(-2282372636672096230),
			countries_iso2 : array('3HzDVinKv2MEYF7B'),
			prize_description : '84hFcotvRjpkQdGH',
			quantity : 47,
			months : 39,
			stars : 8024727220888726260,
			until_date : 30,
		),
		$client->messageMediaGiveawayResults(
			only_new_subscribers : true,
			refunded : true,
			channel_id : -3842783322745528992,
			additional_peers_count : 45,
			launch_msg_id : 61,
			winners_count : 1,
			unclaimed_count : 87,
			winners : array(-5604048345061511194),
			months : 44,
			stars : 5708150165737077487,
			prize_description : '1UnNpgaKBtV6eXlP',
			until_date : 71,
		),
		$client->messageMediaPaidMedia(
			stars_amount : 1790228106739139193,
			extended_media : array(
				$client->messageExtendedMediaPreview(
					w : 71,
					h : 88,
					thumb : $client->photoSizeEmpty(...),
					video_duration : 75,
				),
				$client->messageExtendedMedia(
					media : $client->messageMediaEmpty(...),
				),
			),
		),
		$client->messageMediaToDo(
			todo : $client->todoList(
				others_can_append : true,
				others_can_complete : true,
				title : $client->textWithEntities(...),
				list : array(
					$client->todoItem(...),
				),
			),
			completions : array(
				$client->todoCompletion(
					id : 79,
					completed_by : -6163727222012992172,
					date : 27,
				),
			),
		),
	),
	subscription_period : 62,
	giveaway_post_id : 27,
	stargift : $client->starGift(
		limited : true,
		sold_out : true,
		birthday : true,
		require_premium : true,
		limited_per_user : true,
		id : -8589189876837279597,
		sticker : $client->documentEmpty(
			id : 935980554121796150,
		),
		stars : -6542528193112776677,
		availability_remains : 2,
		availability_total : 39,
		availability_resale : 7170420334509875041,
		convert_stars : -5073843417756832052,
		first_sale_date : 98,
		last_sale_date : 34,
		upgrade_stars : 6353408417586424312,
		resell_min_stars : -451042080719923707,
		title : 'tA1ulsL30F9DYSz4',
		released_by : $client->peerUser(
			user_id : -1936228795593988545,
		),
		per_user_total : 21,
		per_user_remains : 84,
	),
	floodskip_number : 20,
	starref_commission_permille : 30,
	starref_peer : $client->peerUser(
		user_id : -1380898835890284631,
	),
	starref_amount : $client->starsAmount(
		amount : -3090593844080450319,
		nanos : 65,
	),
	paid_messages : 44,
	premium_gift_months : 89,
	ads_proceeds_from_date : 80,
	ads_proceeds_to_date : 59,
);
```