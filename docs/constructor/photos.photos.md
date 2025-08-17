# photos.photos

**Description** : *Full list of photos with auxiliary data*

**Layer** : 211

```tl
photos.photos#8dca6aa5 photos:Vector<Photo> users:Vector<User> = photos.Photos;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>photos</mark> | [`Vector<Photo>`](type/Photo) | List of photos |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of mentioned users |

---

## Type

[photos.Photos](type/photos.Photos)

---

## Example

```php
$photosPhotos = $client->photos->photos(
	photos : array(
		$client->photoEmpty(
			id : -4447903487782480405,
		),
		$client->photo(
			has_stickers : true,
			id : -8560420443120951507,
			access_hash : -346914042743990477,
			file_reference : '??ōfLiveProto:B?X;',
			date : 88,
			sizes : array(
				$client->photoSizeEmpty(
					type : 'RchMFj1N0e79SP84',
				),
				$client->photoSize(
					type : 'pVZI74GA2tuLaTJK',
					w : 73,
					h : 54,
					size : 80,
				),
				$client->photoCachedSize(
					type : 'TW4XPEBiYZmH2dxv',
					w : 24,
					h : 20,
					bytes : '	4?3fLiveProto??q?e',
				),
				$client->photoStrippedSize(
					type : 'dHLr1u7nPkRbyl3J',
					bytes : 'N??)LiveProto%y?~',
				),
				$client->photoSizeProgressive(
					type : 'rKRULsBf5AYCoap9',
					w : 5,
					h : 56,
					sizes : array(29),
				),
				$client->photoPathSize(
					type : 'Aj2o8bwJKEFdWpS7',
					bytes : '??LiveProto?Er?',
				),
			),
			video_sizes : array(
				$client->videoSize(
					type : 'wjTZWV6PI5cknFoH',
					w : 61,
					h : 9,
					size : 40,
					video_start_ts : 423485.8369140625,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 9017643902092570853,
					background_colors : array(16),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -7160593672851380727,
					background_colors : array(47),
				),
			),
			dc_id : 31,
		),
	),
	users : array(
		$client->userEmpty(
			id : -4578300481704672699,
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
			id : 3208787372230891702,
			access_hash : 7106818034602375808,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 62,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'lXCZaf3BWMDOQUP9',
					reason : 'HLOBGbDCX4Qs8e1Y',
					text : '3x0fj7nOvhW2weuy',
				),
			),
			bot_inline_placeholder : '9TgzaslmYh8cfBoQ',
			lang_code : 'OlXBWYF361spNbZG',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 18,
			color : $client->peerColor(
				color : 64,
				background_emoji_id : 5601593873595280225,
			),
			profile_color : $client->peerColor(
				color : 34,
				background_emoji_id : -3446440898379181384,
			),
			bot_active_users : 33,
			bot_verification_icon : -93307082760908437,
			send_paid_messages_stars : 5603005278574639037,
		),
	),
);
```