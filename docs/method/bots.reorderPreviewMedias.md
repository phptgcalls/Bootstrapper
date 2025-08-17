# bots.reorderPreviewMedias

**Description** : *Reorder a main mini app previews, see here » for more info*

**Layer** : 211

```tl
bots.reorderPreviewMedias#b627f3aa bot:InputUser lang_code:string order:Vector<InputMedia> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>bot</mark> | [`InputUser`](type/InputUser) | The bot that owns the Main Mini App |
| <mark>lang_code</mark> | [`string`](type/string) | ISO 639-1 language code, indicating the localization of the previews to reorder |
| <mark>order</mark> | [`Vector<InputMedia>`](type/InputMedia) | New order of the previews |

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
$bool = $client->bots->reorderPreviewMedias(
	bot : $client->inputUserEmpty(),
	lang_code : 'fnMOCq9Tr7IhNBku',
	order : array(
		$client->inputMediaEmpty(),
		$client->inputMediaUploadedPhoto(
			spoiler : true,
			file : $client->inputFile(
				id : 3281160221479543224,
				parts : 31,
				name : 'XsFfml1iYRQW2BCD',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			stickers : array(
				$client->inputDocumentEmpty(),
				$client->inputDocument(
					id : 3285579083069197919,
					access_hash : -6824433876306190738,
					file_reference : '???ϢLiveProto?m2?',
				),
			),
			ttl_seconds : 51,
		),
		$client->inputMediaPhoto(
			spoiler : true,
			id : $client->inputPhotoEmpty(),
			ttl_seconds : 13,
		),
		$client->inputMediaGeoPoint(
			geo_point : $client->inputGeoPointEmpty(),
		),
		$client->inputMediaContact(
			phone_number : '+1234567890',
			first_name : 'Tak',
			last_name : 'None',
			vcard : 'ov1eN3sHEAyt7Klc',
		),
		$client->inputMediaUploadedDocument(
			nosound_video : true,
			force_file : true,
			spoiler : true,
			file : $client->inputFile(
				id : -8463502393125424562,
				parts : 55,
				name : '07M8Er9aBmlydhK1',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			thumb : $client->inputFile(
				id : -7721972724984814229,
				parts : 100,
				name : 'WDcSIXT2bgukxrLY',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			mime_type : 'Xpn9RlPtdBDx5k2U',
			attributes : array(
				$client->documentAttributeImageSize(
					w : 13,
					h : 80,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'aZTzCt4s1HM2FSIl',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 1711423.0517578125,
					w : 37,
					h : 61,
					preload_prefix_size : 98,
					video_start_ts : 1898112.0341796875,
					video_codec : 'KT93HyUDtNzwr8Sh',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 83,
					title : 'lofVjhwNzmWk4BSA',
					performer : '8laXx9NfiOhqCTMG',
					waveform : 'Yj??VLiveProto?o3',
				),
				$client->documentAttributeFilename(
					file_name : '7B2h5iyPfoNKXQwd',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : '6U45kySBspf9hxvi',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
			stickers : array(
				$client->inputDocumentEmpty(),
				$client->inputDocument(
					id : 6775331089926032529,
					access_hash : 1634756592085593203,
					file_reference : '?W7?+LiveProtokL9}',
				),
			),
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 39,
			ttl_seconds : 92,
		),
		$client->inputMediaDocument(
			spoiler : true,
			id : $client->inputDocumentEmpty(),
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 40,
			ttl_seconds : 5,
			query : 'zMTx1mKEsbDtXrZ8',
		),
		$client->inputMediaVenue(
			geo_point : $client->inputGeoPointEmpty(),
			title : 'Y2guS0CGNizFH87D',
			address : 'qQ7dVvcDajyr9T0G',
			provider : '0Gt8wcZ5CHRPpNQ2',
			venue_id : 'QXOUp4csRj56fD0b',
			venue_type : 'PLNhnQ5I8Vx1j6RT',
		),
		$client->inputMediaPhotoExternal(
			spoiler : true,
			url : 'https://docs.liveproto.dev',
			ttl_seconds : 2,
		),
		$client->inputMediaDocumentExternal(
			spoiler : true,
			url : 'https://docs.liveproto.dev',
			ttl_seconds : 54,
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 100,
		),
		$client->inputMediaGame(
			id : $client->inputGameID(
				id : -7512429026144453403,
				access_hash : -4302674094166314069,
			),
		),
		$client->inputMediaInvoice(
			title : 'pU8E7Htmb2yqwRX5',
			description : 'zjMy8s4gOd5bQaSK',
			photo : $client->inputWebDocument(
				url : 'https://docs.liveproto.dev',
				size : 24,
				mime_type : '9CzZIS1TwEUVJerN',
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
				currency : 'TXY4JmECpy9f2AFj',
				prices : array(
					$client->labeledPrice(...),
				),
				max_tip_amount : 5599197250112706481,
				suggested_tip_amounts : array(-2268865057692351092),
				terms_url : 'https://docs.liveproto.dev',
				subscription_period : 68,
			),
			payload : '?o???LiveProto?&??l',
			provider : 'OZzYw3kVHEBof0Sa',
			provider_data : $client->dataJSON(
				data : 'wfDUx92C5tgyurZI',
			),
			start_param : 'a9VxOISL2rznvETm',
			extended_media : $client->inputMediaEmpty(),
		),
		$client->inputMediaGeoLive(
			stopped : true,
			geo_point : $client->inputGeoPointEmpty(),
			heading : 62,
			period : 80,
			proximity_notification_radius : 46,
		),
		$client->inputMediaPoll(
			poll : $client->poll(
				id : -3846884665729456264,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 72,
				close_date : 19,
			),
			correct_answers : array('?8?CLiveProto?u??'),
			solution : 'nlZmLSV6AgKMBxIr',
			solution_entities : array(
				$client->messageEntityUnknown(
					offset : 60,
					length : 80,
				),
				$client->messageEntityMention(
					offset : 81,
					length : 80,
				),
				$client->messageEntityHashtag(
					offset : 80,
					length : 59,
				),
				$client->messageEntityBotCommand(
					offset : 79,
					length : 6,
				),
				$client->messageEntityUrl(
					offset : 22,
					length : 3,
				),
				$client->messageEntityEmail(
					offset : 80,
					length : 70,
				),
				$client->messageEntityBold(
					offset : 2,
					length : 0,
				),
				$client->messageEntityItalic(
					offset : 27,
					length : 43,
				),
				$client->messageEntityCode(
					offset : 39,
					length : 59,
				),
				$client->messageEntityPre(
					offset : 87,
					length : 12,
					language : 'V1FM5eCHIvjynNf9',
				),
				$client->messageEntityTextUrl(
					offset : 35,
					length : 92,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 16,
					length : 13,
					user_id : -3871528618666108047,
				),
				$client->inputMessageEntityMentionName(
					offset : 16,
					length : 58,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 36,
					length : 4,
				),
				$client->messageEntityCashtag(
					offset : 11,
					length : 55,
				),
				$client->messageEntityUnderline(
					offset : 22,
					length : 33,
				),
				$client->messageEntityStrike(
					offset : 86,
					length : 57,
				),
				$client->messageEntityBankCard(
					offset : 10,
					length : 29,
				),
				$client->messageEntitySpoiler(
					offset : 74,
					length : 85,
				),
				$client->messageEntityCustomEmoji(
					offset : 82,
					length : 88,
					document_id : 4247700916938625416,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 45,
					length : 96,
				),
			),
		),
		$client->inputMediaDice(
			emoticon : '8Uarb5L2zOSmvwyA',
		),
		$client->inputMediaStory(
			peer : $client->inputPeerEmpty(),
			id : 13,
		),
		$client->inputMediaWebPage(
			force_large_media : true,
			force_small_media : true,
			optional : true,
			url : 'https://docs.liveproto.dev',
		),
		$client->inputMediaPaidMedia(
			stars_amount : -5219629886549584170,
			extended_media : array(
				$client->inputMediaEmpty(),
				$client->inputMediaUploadedPhoto(
					spoiler : true,
					file : $client->inputFile(...),
					stickers : array(
						$client->inputDocumentEmpty(...),
						$client->inputDocument(...),
					),
					ttl_seconds : 84,
				),
				$client->inputMediaPhoto(
					spoiler : true,
					id : $client->inputPhotoEmpty(...),
					ttl_seconds : 90,
				),
				$client->inputMediaGeoPoint(
					geo_point : $client->inputGeoPointEmpty(...),
				),
				$client->inputMediaContact(
					phone_number : '+1234567890',
					first_name : 'Tak',
					last_name : 'None',
					vcard : 'FjwZH2gDotplIicY',
				),
				$client->inputMediaUploadedDocument(
					nosound_video : true,
					force_file : true,
					spoiler : true,
					file : $client->inputFile(...),
					thumb : $client->inputFile(...),
					mime_type : 'qXOAUSgyHu4Ftz3w',
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
					video_timestamp : 56,
					ttl_seconds : 72,
				),
				$client->inputMediaDocument(
					spoiler : true,
					id : $client->inputDocumentEmpty(...),
					video_cover : $client->inputPhotoEmpty(...),
					video_timestamp : 73,
					ttl_seconds : 76,
					query : 'QAj07nFaoO3eY16H',
				),
				$client->inputMediaVenue(
					geo_point : $client->inputGeoPointEmpty(...),
					title : 'dFznEctjSusMhWfO',
					address : 'gtW7SQ6LGD5FE8wm',
					provider : '9czFYkPt7AHOh8np',
					venue_id : '02oN9itFYJzWZ8QT',
					venue_type : 'kBox7HjnKcItZDMC',
				),
				$client->inputMediaPhotoExternal(
					spoiler : true,
					url : 'https://docs.liveproto.dev',
					ttl_seconds : 8,
				),
				$client->inputMediaDocumentExternal(
					spoiler : true,
					url : 'https://docs.liveproto.dev',
					ttl_seconds : 39,
					video_cover : $client->inputPhotoEmpty(...),
					video_timestamp : 78,
				),
				$client->inputMediaGame(
					id : $client->inputGameID(...),
				),
				$client->inputMediaInvoice(
					title : 'JF2QUaP9OCT4mBKZ',
					description : '1tMu8EBHW53w6ALz',
					photo : $client->inputWebDocument(...),
					invoice : $client->invoice(...),
					payload : 'Z`??LiveProtod??¯',
					provider : 'BR0HP129JZd6OEwq',
					provider_data : $client->dataJSON(...),
					start_param : 'FpS6kDz5GhiI8By9',
					extended_media : $client->inputMediaEmpty(...),
				),
				$client->inputMediaGeoLive(
					stopped : true,
					geo_point : $client->inputGeoPointEmpty(...),
					heading : 37,
					period : 79,
					proximity_notification_radius : 19,
				),
				$client->inputMediaPoll(
					poll : $client->poll(...),
					correct_answers : array('??m?YLiveProtog?~?'),
					solution : 'MUbqSkZK0oswxICA',
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
					emoticon : 'C1uXtBm5kqLjf7EK',
				),
				$client->inputMediaStory(
					peer : $client->inputPeerEmpty(...),
					id : 24,
				),
				$client->inputMediaWebPage(
					force_large_media : true,
					force_small_media : true,
					optional : true,
					url : 'https://docs.liveproto.dev',
				),
				$client->inputMediaPaidMedia(
					stars_amount : -1437895938338860906,
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
					payload : 'HJoeklr4SiGzxWqB',
				),
				$client->inputMediaTodo(
					todo : $client->todoList(...),
				),
			),
			payload : 'alfTGCkpAWrDUB1E',
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