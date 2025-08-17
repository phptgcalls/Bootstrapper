# photos.photosSlice

**Description** : *Incomplete list of photos with auxiliary data*

**Layer** : 211

```tl
photos.photosSlice#15051f54 count:int photos:Vector<Photo> users:Vector<User> = photos.Photos;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Total number of photos |
| <mark>photos</mark> | [`Vector<Photo>`](type/Photo) | List of photos |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of mentioned users |

---

## Type

[photos.Photos](type/photos.Photos)

---

## Example

```php
$photosPhotos = $client->photos->photosSlice(
	count : 52,
	photos : array(
		$client->photoEmpty(
			id : 4055590308919056146,
		),
		$client->photo(
			has_stickers : true,
			id : -3339104297785230356,
			access_hash : 3360681423461025682,
			file_reference : '??aaLiveProto??%?',
			date : 24,
			sizes : array(
				$client->photoSizeEmpty(
					type : 'Wf3GaTp72KvE8zeI',
				),
				$client->photoSize(
					type : 'hmi5ETNgbXq3u4yt',
					w : 87,
					h : 29,
					size : 63,
				),
				$client->photoCachedSize(
					type : 'd2JkwgV7aUmPKx4r',
					w : 49,
					h : 62,
					bytes : '?f??LiveProto~?\'',
				),
				$client->photoStrippedSize(
					type : 'R65sy8z4JlAUpNxX',
					bytes : '?ǉ?LiveProtoW??',
				),
				$client->photoSizeProgressive(
					type : 'sjnmiX8MWDF6RNEV',
					w : 93,
					h : 87,
					sizes : array(32),
				),
				$client->photoPathSize(
					type : 'IeZbhwi01MCXWRsk',
					bytes : 'x??XLiveProto0U??',
				),
			),
			video_sizes : array(
				$client->videoSize(
					type : 'Lz5gnC1KM7YGipDT',
					w : 88,
					h : 9,
					size : 68,
					video_start_ts : -1980818.236328125,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 2362470045254915975,
					background_colors : array(47),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 3522946507418186640,
					background_colors : array(21),
				),
			),
			dc_id : 2,
		),
	),
	users : array(
		$client->userEmpty(
			id : -4753624370558647874,
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
			id : -1030391589337305730,
			access_hash : 2787324584019033457,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 73,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Fo3ScyN9eRqPtn1M',
					reason : 'KOgCIoMBXv0VEkY4',
					text : 'bzui3KOyBdeV1QW2',
				),
			),
			bot_inline_placeholder : 'Q2SYWC9EftIsKzAg',
			lang_code : 'Nu4eWb6PgjMRkFLc',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 47,
			color : $client->peerColor(
				color : 70,
				background_emoji_id : 912548986979186835,
			),
			profile_color : $client->peerColor(
				color : 37,
				background_emoji_id : -7229695625634263500,
			),
			bot_active_users : 31,
			bot_verification_icon : 854554805830379362,
			send_paid_messages_stars : 6912044833487289607,
		),
	),
);
```