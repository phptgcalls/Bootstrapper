# help.premiumPromo

**Description** : *Telegram Premium promotion information*

**Layer** : 211

```tl
help.premiumPromo#5334759c status_text:string status_entities:Vector<MessageEntity> video_sections:Vector<string> videos:Vector<Document> period_options:Vector<PremiumSubscriptionOption> users:Vector<User> = help.PremiumPromo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>status_text</mark> | [`string`](type/string) | Description of the current state of the user's Telegram Premium subscription |
| <mark>status_entities</mark> | [`Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| <mark>video_sections</mark> | [`Vector<string>`](type/string) | A list of premium feature identifiers », associated to each video |
| <mark>videos</mark> | [`Vector<Document>`](type/Document) | A list of videos |
| <mark>period_options</mark> | [`Vector<PremiumSubscriptionOption>`](type/PremiumSubscriptionOption) | Telegram Premium subscription options |
| <mark>users</mark> | [`Vector<User>`](type/User) | Related user information |

---

## Type

[help.PremiumPromo](type/help.PremiumPromo)

---

## Example

```php
$helpPremiumPromo = $client->help->premiumPromo(
	status_text : 'GWgljzHQk5rPDo8q',
	status_entities : array(
		$client->messageEntityUnknown(
			offset : 3,
			length : 84,
		),
		$client->messageEntityMention(
			offset : 47,
			length : 30,
		),
		$client->messageEntityHashtag(
			offset : 82,
			length : 67,
		),
		$client->messageEntityBotCommand(
			offset : 81,
			length : 39,
		),
		$client->messageEntityUrl(
			offset : 16,
			length : 29,
		),
		$client->messageEntityEmail(
			offset : 73,
			length : 9,
		),
		$client->messageEntityBold(
			offset : 35,
			length : 25,
		),
		$client->messageEntityItalic(
			offset : 95,
			length : 13,
		),
		$client->messageEntityCode(
			offset : 30,
			length : 13,
		),
		$client->messageEntityPre(
			offset : 22,
			length : 53,
			language : 'oknh8LZTy4dtWKGU',
		),
		$client->messageEntityTextUrl(
			offset : 89,
			length : 56,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 100,
			length : 31,
			user_id : 9183764448121379508,
		),
		$client->inputMessageEntityMentionName(
			offset : 3,
			length : 42,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 29,
			length : 60,
		),
		$client->messageEntityCashtag(
			offset : 37,
			length : 5,
		),
		$client->messageEntityUnderline(
			offset : 72,
			length : 38,
		),
		$client->messageEntityStrike(
			offset : 63,
			length : 9,
		),
		$client->messageEntityBankCard(
			offset : 29,
			length : 19,
		),
		$client->messageEntitySpoiler(
			offset : 0,
			length : 43,
		),
		$client->messageEntityCustomEmoji(
			offset : 78,
			length : 67,
			document_id : 7318118367503137242,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 76,
			length : 1,
		),
	),
	video_sections : array('g48G2Tq79jvdHerY'),
	videos : array(
		$client->documentEmpty(
			id : 8899897662393185758,
		),
		$client->document(
			id : 6818065547727362160,
			access_hash : -1143464969671804141,
			file_reference : '???OLiveProto?GZ?',
			date : 17,
			mime_type : 'N9JX2ZEgGwos5Drd',
			size : -705132380850072835,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'DgVJNU1B4ymjob25',
				),
				$client->photoSize(
					type : 'mrBoqCeb1ZcMDf2s',
					w : 30,
					h : 47,
					size : 34,
				),
				$client->photoCachedSize(
					type : 'npdRgYKrels598ZH',
					w : 14,
					h : 47,
					bytes : '"A:hLiveProto??ȸ',
				),
				$client->photoStrippedSize(
					type : 'MLr5lGYWJ6EpvIPB',
					bytes : '?]?LiveProto?6??',
				),
				$client->photoSizeProgressive(
					type : '4TnPN2xrCABYcykj',
					w : 71,
					h : 44,
					sizes : array(22),
				),
				$client->photoPathSize(
					type : '8KuHp9G7OiBMeVqb',
					bytes : '5w??LiveProto)`V??',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : '8YZswNn2KriUW0Lk',
					w : 76,
					h : 70,
					size : 22,
					video_start_ts : 787563.9716796875,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 2415319354463986636,
					background_colors : array(73),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -2059381359502511300,
					background_colors : array(50),
				),
			),
			dc_id : 37,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 68,
					h : 62,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'QUmJrLcKFk4OZn2Y',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 200403.3232421875,
					w : 18,
					h : 12,
					preload_prefix_size : 91,
					video_start_ts : -744238.357421875,
					video_codec : 'Om1RZHAMvkBQJEel',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 73,
					title : 'vBxjUT7qR39cikQz',
					performer : 'ZzJQiqcImhOFPgv2',
					waveform : '?5?LiveProtoa]Fn?',
				),
				$client->documentAttributeFilename(
					file_name : 'XcDgzixEVA3L5HkB',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'uqHx8ioJmQk5tS2f',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
	period_options : array(
		$client->premiumSubscriptionOption(
			current : true,
			can_purchase_upgrade : true,
			transaction : 'S3gLqbrVOH2tjK5e',
			months : 16,
			currency : 'Zyl1MUhnWfqvrdga',
			amount : -4251794472229651141,
			bot_url : 'https://docs.liveproto.dev',
			store_product : '3osGg8DANYjnbZi1',
		),
	),
	users : array(
		$client->userEmpty(
			id : -5126027801173813655,
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
			id : -6910488554569229020,
			access_hash : -3272159173850893234,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 32,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Ci5sA3MfbTDYHUP1',
					reason : 'iNmFIMd1WXkYLSnh',
					text : 'kCKIa0jNTFeUn3lW',
				),
			),
			bot_inline_placeholder : 'MnqCd42W3cXtDeZB',
			lang_code : 'u3TC5biVXeD1R7M4',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 63,
			color : $client->peerColor(
				color : 37,
				background_emoji_id : -9024473537743045653,
			),
			profile_color : $client->peerColor(
				color : 18,
				background_emoji_id : 681561977010325836,
			),
			bot_active_users : 25,
			bot_verification_icon : 3267931195450123833,
			send_paid_messages_stars : 1394943828418113745,
		),
	),
);
```