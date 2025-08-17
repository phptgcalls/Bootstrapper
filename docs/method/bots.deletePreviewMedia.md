# bots.deletePreviewMedia

**Description** : *Delete a main mini app preview, see here » for more info*

**Layer** : 211

```tl
bots.deletePreviewMedia#2d0135b3 bot:InputUser lang_code:string media:Vector<InputMedia> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>bot</mark> | [`InputUser`](type/InputUser) | The bot that owns the Main Mini App |
| <mark>lang_code</mark> | [`string`](type/string) | ISO 639-1 language code, indicating the localization of the preview to delete |
| <mark>media</mark> | [`Vector<InputMedia>`](type/InputMedia) | The photo/video preview to delete, previously fetched as specified here » |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **BOT_INVALID** | `400` | This is not a valid bot |

---

## Example

```php
$bool = $client->bots->deletePreviewMedia(
	bot : $client->inputUserEmpty(),
	lang_code : 'zLP6IgynceE5dDfG',
	media : array(
		$client->inputMediaEmpty(),
		$client->inputMediaUploadedPhoto(
			spoiler : true,
			file : $client->inputFile(
				id : 7737168205792856855,
				parts : 93,
				name : 'KmPgVW2azSwsQfo4',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			stickers : array(
				$client->inputDocumentEmpty(),
				$client->inputDocument(
					id : -5465720410084522518,
					access_hash : -6800249497940337899,
					file_reference : '???LiveProto??g1B',
				),
			),
			ttl_seconds : 20,
		),
		$client->inputMediaPhoto(
			spoiler : true,
			id : $client->inputPhotoEmpty(),
			ttl_seconds : 26,
		),
		$client->inputMediaGeoPoint(
			geo_point : $client->inputGeoPointEmpty(),
		),
		$client->inputMediaContact(
			phone_number : '+1234567890',
			first_name : 'Tak',
			last_name : 'None',
			vcard : 'Q4h8N0VJyqZ9TtdM',
		),
		$client->inputMediaUploadedDocument(
			nosound_video : true,
			force_file : true,
			spoiler : true,
			file : $client->inputFile(
				id : 1627046043675249408,
				parts : 60,
				name : '8RYvwU3bXlPZsEAj',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			thumb : $client->inputFile(
				id : 4845297725748593821,
				parts : 21,
				name : 'FJLsUKQB1ZaWpRkt',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			mime_type : 'QIPofUeYdmVOb0jX',
			attributes : array(
				$client->documentAttributeImageSize(
					w : 85,
					h : 76,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'qs0T3tpUQ8wAiLmE',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 595372.748046875,
					w : 82,
					h : 53,
					preload_prefix_size : 7,
					video_start_ts : -1590094.4833984375,
					video_codec : 'B1oTtluSgUI6OjpN',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 22,
					title : 'NtU9DsV1RKXPjHcp',
					performer : 'S0xXhBaqmfDGKdEo',
					waveform : ')t?UDLiveProto??;??',
				),
				$client->documentAttributeFilename(
					file_name : '6RJD5Btmw3y8Tu4U',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'gJX7DQoxKGOjlq2F',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
			stickers : array(
				$client->inputDocumentEmpty(),
				$client->inputDocument(
					id : 8823412555617084498,
					access_hash : -6484741520521105786,
					file_reference : '?S42LiveProto*4	#?',
				),
			),
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 97,
			ttl_seconds : 82,
		),
		$client->inputMediaDocument(
			spoiler : true,
			id : $client->inputDocumentEmpty(),
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 35,
			ttl_seconds : 79,
			query : 'DOKtavMuX7qpJIlk',
		),
		$client->inputMediaVenue(
			geo_point : $client->inputGeoPointEmpty(),
			title : 'oxgaup9qne4Kj7tb',
			address : 'fU5FuR0Xyojlm9pz',
			provider : 'B7UpXPWi2yE5INYg',
			venue_id : '9dq3e1DLycHafpog',
			venue_type : 'BQaOwUWuchC6IgVZ',
		),
		$client->inputMediaPhotoExternal(
			spoiler : true,
			url : 'https://docs.liveproto.dev',
			ttl_seconds : 21,
		),
		$client->inputMediaDocumentExternal(
			spoiler : true,
			url : 'https://docs.liveproto.dev',
			ttl_seconds : 57,
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 46,
		),
		$client->inputMediaGame(
			id : $client->inputGameID(
				id : -1103464878865705559,
				access_hash : 4945999280816276681,
			),
		),
		$client->inputMediaInvoice(
			title : 'b1ZKP27OaVxCrkwu',
			description : 'xuICRWJ7KNVtQ8Yb',
			photo : $client->inputWebDocument(
				url : 'https://docs.liveproto.dev',
				size : 10,
				mime_type : '0aNLZyeEiOxwCDWS',
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
			invoice : $client->invoice(
				test : true,
				name_requested : true,
				phone_requested : true,
				email_requested : true,
				shipping_address_requested : true,
				flexible : true,
				phone_to_provider : true,
				email_to_provider : true,
				recurring : true,
				currency : '7lgeqBIvt1OLZ58n',
				prices : array(
					$client->labeledPrice(...),
				),
				max_tip_amount : 2358627531452095347,
				suggested_tip_amounts : array(-1490562566713799567),
				terms_url : 'https://docs.liveproto.dev',
				subscription_period : 89,
			),
			payload : '??,??LiveProto-q?4?',
			provider : '1frdSD7vXFLZYxkm',
			provider_data : $client->dataJSON(
				data : 'gHnKB5JQ7sxyNUae',
			),
			start_param : 'uKhkRzOfla2U0CJP',
			extended_media : $client->inputMediaEmpty(),
		),
		$client->inputMediaGeoLive(
			stopped : true,
			geo_point : $client->inputGeoPointEmpty(),
			heading : 50,
			period : 4,
			proximity_notification_radius : 31,
		),
		$client->inputMediaPoll(
			poll : $client->poll(
				id : 8526108374764700934,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 61,
				close_date : 7,
			),
			correct_answers : array('????LiveProto%իv'),
			solution : 'jK0NhSIRoUOfvlia',
			solution_entities : array(
				$client->messageEntityUnknown(
					offset : 95,
					length : 97,
				),
				$client->messageEntityMention(
					offset : 97,
					length : 80,
				),
				$client->messageEntityHashtag(
					offset : 25,
					length : 81,
				),
				$client->messageEntityBotCommand(
					offset : 33,
					length : 71,
				),
				$client->messageEntityUrl(
					offset : 54,
					length : 80,
				),
				$client->messageEntityEmail(
					offset : 10,
					length : 33,
				),
				$client->messageEntityBold(
					offset : 3,
					length : 59,
				),
				$client->messageEntityItalic(
					offset : 17,
					length : 90,
				),
				$client->messageEntityCode(
					offset : 44,
					length : 90,
				),
				$client->messageEntityPre(
					offset : 47,
					length : 57,
					language : 'zSELMb81rq7KHNGY',
				),
				$client->messageEntityTextUrl(
					offset : 90,
					length : 62,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 49,
					length : 63,
					user_id : -2911324398103060165,
				),
				$client->inputMessageEntityMentionName(
					offset : 40,
					length : 65,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 83,
					length : 85,
				),
				$client->messageEntityCashtag(
					offset : 69,
					length : 57,
				),
				$client->messageEntityUnderline(
					offset : 87,
					length : 40,
				),
				$client->messageEntityStrike(
					offset : 13,
					length : 97,
				),
				$client->messageEntityBankCard(
					offset : 46,
					length : 70,
				),
				$client->messageEntitySpoiler(
					offset : 59,
					length : 44,
				),
				$client->messageEntityCustomEmoji(
					offset : 72,
					length : 33,
					document_id : 714480265944312320,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 100,
					length : 55,
				),
			),
		),
		$client->inputMediaDice(
			emoticon : 'soqBTHpavgiOWl8r',
		),
		$client->inputMediaStory(
			peer : $client->inputPeerEmpty(),
			id : 81,
		),
		$client->inputMediaWebPage(
			force_large_media : true,
			force_small_media : true,
			optional : true,
			url : 'https://docs.liveproto.dev',
		),
		$client->inputMediaPaidMedia(
			stars_amount : 3301631949363998475,
			extended_media : array(
				$client->inputMediaEmpty(),
				$client->inputMediaUploadedPhoto(
					spoiler : true,
					file : $client->inputFile(...),
					stickers : array(
						$client->inputDocumentEmpty(...),
						$client->inputDocument(...),
					),
					ttl_seconds : 71,
				),
				$client->inputMediaPhoto(
					spoiler : true,
					id : $client->inputPhotoEmpty(...),
					ttl_seconds : 76,
				),
				$client->inputMediaGeoPoint(
					geo_point : $client->inputGeoPointEmpty(...),
				),
				$client->inputMediaContact(
					phone_number : '+1234567890',
					first_name : 'Tak',
					last_name : 'None',
					vcard : 'F95h4jqclIMJVLe3',
				),
				$client->inputMediaUploadedDocument(
					nosound_video : true,
					force_file : true,
					spoiler : true,
					file : $client->inputFile(...),
					thumb : $client->inputFile(...),
					mime_type : 'rigdfBcDAsRYwPxn',
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
					stickers : array(
						$client->inputDocumentEmpty(...),
						$client->inputDocument(...),
					),
					video_cover : $client->inputPhotoEmpty(...),
					video_timestamp : 4,
					ttl_seconds : 10,
				),
				$client->inputMediaDocument(
					spoiler : true,
					id : $client->inputDocumentEmpty(...),
					video_cover : $client->inputPhotoEmpty(...),
					video_timestamp : 27,
					ttl_seconds : 41,
					query : 'XCmWP7Jzca3i1sZA',
				),
				$client->inputMediaVenue(
					geo_point : $client->inputGeoPointEmpty(...),
					title : '2bdKr0VBlLWQiHoN',
					address : '7vRJq5LZobXFAgIE',
					provider : 'y45B0srjQdgAikVG',
					venue_id : 'KG3IeUJPci2OmWMk',
					venue_type : 'LT6sJ8CV5GOmY0IF',
				),
				$client->inputMediaPhotoExternal(
					spoiler : true,
					url : 'https://docs.liveproto.dev',
					ttl_seconds : 1,
				),
				$client->inputMediaDocumentExternal(
					spoiler : true,
					url : 'https://docs.liveproto.dev',
					ttl_seconds : 29,
					video_cover : $client->inputPhotoEmpty(...),
					video_timestamp : 2,
				),
				$client->inputMediaGame(
					id : $client->inputGameID(...),
				),
				$client->inputMediaInvoice(
					title : 'oCuQytYvJR2nsm7l',
					description : 'AhUQ1Gq6YiloDSe3',
					photo : $client->inputWebDocument(...),
					invoice : $client->invoice(...),
					payload : 'ѫ@C5LiveProto?`Ͱ?',
					provider : '6l7XxYHzmqsZu9Lo',
					provider_data : $client->dataJSON(...),
					start_param : 'UotZ3hYd18albpWe',
					extended_media : $client->inputMediaEmpty(...),
				),
				$client->inputMediaGeoLive(
					stopped : true,
					geo_point : $client->inputGeoPointEmpty(...),
					heading : 93,
					period : 95,
					proximity_notification_radius : 97,
				),
				$client->inputMediaPoll(
					poll : $client->poll(...),
					correct_answers : array('
??LiveProto&?!??'),
					solution : 'cIbN3JYVRWmUqkef',
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
				$client->inputMediaDice(
					emoticon : 'oEB69wHfxl2IaDPR',
				),
				$client->inputMediaStory(
					peer : $client->inputPeerEmpty(...),
					id : 94,
				),
				$client->inputMediaWebPage(
					force_large_media : true,
					force_small_media : true,
					optional : true,
					url : 'https://docs.liveproto.dev',
				),
				$client->inputMediaPaidMedia(
					stars_amount : -6463259313088503595,
					extended_media : array(
						$client->inputMediaEmpty(...),
						$client->inputMediaUploadedPhoto(...),
						$client->inputMediaPhoto(...),
						$client->inputMediaGeoPoint(...),
						$client->inputMediaContact(...),
						$client->inputMediaUploadedDocument(...),
						$client->inputMediaDocument(...),
						$client->inputMediaVenue(...),
						$client->inputMediaPhotoExternal(...),
						$client->inputMediaDocumentExternal(...),
						$client->inputMediaGame(...),
						$client->inputMediaInvoice(...),
						$client->inputMediaGeoLive(...),
						$client->inputMediaPoll(...),
						$client->inputMediaDice(...),
						$client->inputMediaStory(...),
						$client->inputMediaWebPage(...),
						$client->inputMediaPaidMedia(...),
						$client->inputMediaTodo(...),
					),
					payload : 'HpZ3YLG2FN1IXzhr',
				),
				$client->inputMediaTodo(
					todo : $client->todoList(...),
				),
			),
			payload : 'JV9Bh1zKlvj42Gyt',
		),
		$client->inputMediaTodo(
			todo : $client->todoList(
				others_can_append : true,
				others_can_complete : true,
				title : $client->textWithEntities(...),
				list : array(
					$client->todoItem(...),
				),
			),
		),
	),
);
```