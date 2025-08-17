# inputMediaPaidMedia

**Description** : *Paid media, see here » for more info*

**Layer** : 211

```tl
inputMediaPaidMedia#c4103386 flags:# stars_amount:long extended_media:Vector<InputMedia> payload:flags.0?string = InputMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>stars_amount</mark> | [`long`](type/long) | The price of the media in Telegram Stars |
| <mark>extended_media</mark> | [`Vector<InputMedia>`](type/InputMedia) | Photos or videos |
| **payload** | [`flags.0?string`](type/string) | Bots only, specifies a custom payload that will then be passed in updateBotPurchasedPaidMedia when a payment is made (this field will not be visible to the user) |

---

## Type

[InputMedia](type/InputMedia)

---

## Example

```php
$inputMedia = $client->inputMediaPaidMedia(
	stars_amount : -4942259434982970608,
	extended_media : array(
		$client->inputMediaEmpty(),
		$client->inputMediaUploadedPhoto(
			spoiler : true,
			file : $client->inputFile(
				id : -8716436416611216003,
				parts : 97,
				name : 'rnwoSYGUxcHjLPX2',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			stickers : array(
				$client->inputDocumentEmpty(),
				$client->inputDocument(
					id : -7464345004207433961,
					access_hash : -1839512576902687105,
					file_reference : '?Km>?LiveProto[??(?',
				),
			),
			ttl_seconds : 50,
		),
		$client->inputMediaPhoto(
			spoiler : true,
			id : $client->inputPhotoEmpty(),
			ttl_seconds : 44,
		),
		$client->inputMediaGeoPoint(
			geo_point : $client->inputGeoPointEmpty(),
		),
		$client->inputMediaContact(
			phone_number : '+1234567890',
			first_name : 'Tak',
			last_name : 'None',
			vcard : 'RQ6xbln3eCr75fkd',
		),
		$client->inputMediaUploadedDocument(
			nosound_video : true,
			force_file : true,
			spoiler : true,
			file : $client->inputFile(
				id : -4580769195121944457,
				parts : 42,
				name : 'k9SptRgUvC3b5WaA',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			thumb : $client->inputFile(
				id : -3124878726477039069,
				parts : 6,
				name : 'FNawzvrJo4KyWuTH',
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			),
			mime_type : 'IibquJUyRzt9Tf4P',
			attributes : array(
				$client->documentAttributeImageSize(
					w : 95,
					h : 13,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'E5zTs3H4nSd8yArh',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 1718605.302734375,
					w : 61,
					h : 25,
					preload_prefix_size : 99,
					video_start_ts : -1007159.8505859375,
					video_codec : '8sEh5JnOzm7ugISe',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 9,
					title : 'SHp37OM20FDwEQPv',
					performer : 'AlEMuRCGQq1c5ysw',
					waveform : '?3oLiveProto?n?m',
				),
				$client->documentAttributeFilename(
					file_name : 'YxEbUdiNlyWsABm8',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : '6eYzcX8fRFuKNaWH',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
			stickers : array(
				$client->inputDocumentEmpty(),
				$client->inputDocument(
					id : -4195072005494485765,
					access_hash : -5657208249541148985,
					file_reference : '?H3?LiveProto#xE?',
				),
			),
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 70,
			ttl_seconds : 44,
		),
		$client->inputMediaDocument(
			spoiler : true,
			id : $client->inputDocumentEmpty(),
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 50,
			ttl_seconds : 54,
			query : 'VP7HQND8qz6yeLC0',
		),
		$client->inputMediaVenue(
			geo_point : $client->inputGeoPointEmpty(),
			title : 'mnME6yoxTBZOszSQ',
			address : 'SupmKREIFOjQ814G',
			provider : 'j75SlruR6GD2dZtW',
			venue_id : 'A7OX6M4axnLfPrKQ',
			venue_type : 'iTGxCuezVrtcsboX',
		),
		$client->inputMediaPhotoExternal(
			spoiler : true,
			url : 'https://docs.liveproto.dev',
			ttl_seconds : 85,
		),
		$client->inputMediaDocumentExternal(
			spoiler : true,
			url : 'https://docs.liveproto.dev',
			ttl_seconds : 12,
			video_cover : $client->inputPhotoEmpty(),
			video_timestamp : 96,
		),
		$client->inputMediaGame(
			id : $client->inputGameID(
				id : 5406481203157217657,
				access_hash : -7466144353164162500,
			),
		),
		$client->inputMediaInvoice(
			title : 'qVSDa2fQX6Z0mRBw',
			description : 'hr6i4fNGPvUH9XeT',
			photo : $client->inputWebDocument(
				url : 'https://docs.liveproto.dev',
				size : 67,
				mime_type : 'YQynM3rfeG6EU245',
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
				currency : 'e3SWnK6EwGBk0vDg',
				prices : array(
					$client->labeledPrice(...),
				),
				max_tip_amount : 5807112109250292285,
				suggested_tip_amounts : array(7674279620551009962),
				terms_url : 'https://docs.liveproto.dev',
				subscription_period : 70,
			),
			payload : 'F?r?LiveProto޶??',
			provider : 'ylZETunsG65LSP8m',
			provider_data : $client->dataJSON(
				data : 'PcLsryaNFbpzdgqj',
			),
			start_param : 'FcKiXjewaRYT92LH',
			extended_media : $client->inputMediaEmpty(),
		),
		$client->inputMediaGeoLive(
			stopped : true,
			geo_point : $client->inputGeoPointEmpty(),
			heading : 97,
			period : 88,
			proximity_notification_radius : 40,
		),
		$client->inputMediaPoll(
			poll : $client->poll(
				id : 5671452887966591491,
				closed : true,
				public_voters : true,
				multiple_choice : true,
				quiz : true,
				question : $client->textWithEntities(...),
				answers : array(
					$client->pollAnswer(...),
				),
				close_period : 99,
				close_date : 88,
			),
			correct_answers : array('??H+LiveProto	??W('),
			solution : 'Rrpb3G1CQEh9eXfB',
			solution_entities : array(
				$client->messageEntityUnknown(
					offset : 61,
					length : 92,
				),
				$client->messageEntityMention(
					offset : 19,
					length : 60,
				),
				$client->messageEntityHashtag(
					offset : 68,
					length : 41,
				),
				$client->messageEntityBotCommand(
					offset : 10,
					length : 26,
				),
				$client->messageEntityUrl(
					offset : 12,
					length : 31,
				),
				$client->messageEntityEmail(
					offset : 47,
					length : 13,
				),
				$client->messageEntityBold(
					offset : 79,
					length : 68,
				),
				$client->messageEntityItalic(
					offset : 9,
					length : 56,
				),
				$client->messageEntityCode(
					offset : 60,
					length : 73,
				),
				$client->messageEntityPre(
					offset : 44,
					length : 66,
					language : 'hZcaTmKUEdQflAvt',
				),
				$client->messageEntityTextUrl(
					offset : 17,
					length : 40,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 49,
					length : 68,
					user_id : 2222332656624481880,
				),
				$client->inputMessageEntityMentionName(
					offset : 32,
					length : 9,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 96,
					length : 60,
				),
				$client->messageEntityCashtag(
					offset : 79,
					length : 41,
				),
				$client->messageEntityUnderline(
					offset : 59,
					length : 43,
				),
				$client->messageEntityStrike(
					offset : 1,
					length : 97,
				),
				$client->messageEntityBankCard(
					offset : 11,
					length : 62,
				),
				$client->messageEntitySpoiler(
					offset : 60,
					length : 53,
				),
				$client->messageEntityCustomEmoji(
					offset : 73,
					length : 19,
					document_id : 7824119853621552740,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 99,
					length : 84,
				),
			),
		),
		$client->inputMediaDice(
			emoticon : 'DZEdtNWp3T58Oyo7',
		),
		$client->inputMediaStory(
			peer : $client->inputPeerEmpty(),
			id : 65,
		),
		$client->inputMediaWebPage(
			force_large_media : true,
			force_small_media : true,
			optional : true,
			url : 'https://docs.liveproto.dev',
		),
		$client->inputMediaPaidMedia(
			stars_amount : 5486343265039401331,
			extended_media : array(
				$client->inputMediaEmpty(),
				$client->inputMediaUploadedPhoto(
					spoiler : true,
					file : $client->inputFile(...),
					stickers : array(
						$client->inputDocumentEmpty(...),
						$client->inputDocument(...),
					),
					ttl_seconds : 60,
				),
				$client->inputMediaPhoto(
					spoiler : true,
					id : $client->inputPhotoEmpty(...),
					ttl_seconds : 1,
				),
				$client->inputMediaGeoPoint(
					geo_point : $client->inputGeoPointEmpty(...),
				),
				$client->inputMediaContact(
					phone_number : '+1234567890',
					first_name : 'Tak',
					last_name : 'None',
					vcard : 'H2TK3vIdlNhwLsJ9',
				),
				$client->inputMediaUploadedDocument(
					nosound_video : true,
					force_file : true,
					spoiler : true,
					file : $client->inputFile(...),
					thumb : $client->inputFile(...),
					mime_type : 'yVdSQp39ZA1R8LXF',
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
					video_timestamp : 64,
					ttl_seconds : 80,
				),
				$client->inputMediaDocument(
					spoiler : true,
					id : $client->inputDocumentEmpty(...),
					video_cover : $client->inputPhotoEmpty(...),
					video_timestamp : 83,
					ttl_seconds : 39,
					query : 'TNxPD9CRLOh4GZ2m',
				),
				$client->inputMediaVenue(
					geo_point : $client->inputGeoPointEmpty(...),
					title : 'w6NSYD3gfCUGuHdE',
					address : 'lXe8S2z6iLNcJFGK',
					provider : 'YkDMTvadBch7AK8H',
					venue_id : 'YcwuVNExRjWMKqy7',
					venue_type : 'DwUZ3ukKsLGf5tRI',
				),
				$client->inputMediaPhotoExternal(
					spoiler : true,
					url : 'https://docs.liveproto.dev',
					ttl_seconds : 31,
				),
				$client->inputMediaDocumentExternal(
					spoiler : true,
					url : 'https://docs.liveproto.dev',
					ttl_seconds : 53,
					video_cover : $client->inputPhotoEmpty(...),
					video_timestamp : 85,
				),
				$client->inputMediaGame(
					id : $client->inputGameID(...),
				),
				$client->inputMediaInvoice(
					title : 'UPJfdDwyapk5YNm4',
					description : 'vcuNmWH3CrgZPsb5',
					photo : $client->inputWebDocument(...),
					invoice : $client->invoice(...),
					payload : '1:_?WLiveProto??^?',
					provider : 'o1bAGKOkUInvec0a',
					provider_data : $client->dataJSON(...),
					start_param : 'JwtrL3VX7Wc9NGib',
					extended_media : $client->inputMediaEmpty(...),
				),
				$client->inputMediaGeoLive(
					stopped : true,
					geo_point : $client->inputGeoPointEmpty(...),
					heading : 20,
					period : 15,
					proximity_notification_radius : 65,
				),
				$client->inputMediaPoll(
					poll : $client->poll(...),
					correct_answers : array('ט?(LiveProto???D9'),
					solution : 'Ss2869DXArfpYBRe',
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
					emoticon : 'FSpgPWHoeMCwGBqJ',
				),
				$client->inputMediaStory(
					peer : $client->inputPeerEmpty(...),
					id : 52,
				),
				$client->inputMediaWebPage(
					force_large_media : true,
					force_small_media : true,
					optional : true,
					url : 'https://docs.liveproto.dev',
				),
				$client->inputMediaPaidMedia(
					stars_amount : -1745959050125850473,
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
					payload : 'XhWDGALMfdOt6wE5',
				),
				$client->inputMediaTodo(
					todo : $client->todoList(...),
				),
			),
			payload : 'tUZIl4h6ux0mpVSi',
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
	payload : 'F92XrAdZpyweh3bG',
);
```