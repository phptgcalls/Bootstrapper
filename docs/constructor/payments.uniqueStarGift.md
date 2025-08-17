# payments.uniqueStarGift

**Layer** : 211

```tl
payments.uniqueStarGift#caa2f60b gift:StarGift users:Vector<User> = payments.UniqueStarGift;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>gift</mark> | [`StarGift`](type/StarGift) | NOTHING |
| <mark>users</mark> | [`Vector<User>`](type/User) | NOTHING |

---

## Type

[payments.UniqueStarGift](type/payments.UniqueStarGift)

---

## Example

```php
$paymentsUniqueStarGift = $client->payments->uniqueStarGift(
	gift : $client->starGift(
		limited : true,
		sold_out : true,
		birthday : true,
		require_premium : true,
		limited_per_user : true,
		id : -6767848924959477462,
		sticker : $client->documentEmpty(
			id : 8997810267148208262,
		),
		stars : -4536779554051978931,
		availability_remains : 88,
		availability_total : 8,
		availability_resale : -8747890266185796611,
		convert_stars : 786441600939857104,
		first_sale_date : 11,
		last_sale_date : 31,
		upgrade_stars : -951024377755014600,
		resell_min_stars : 5675124523177157731,
		title : 'guoPC2FkxAV7H0w9',
		released_by : $client->peerUser(
			user_id : 2800890242758761202,
		),
		per_user_total : 1,
		per_user_remains : 65,
	),
	users : array(
		$client->userEmpty(
			id : 8650260252435674077,
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
			id : -7372120499944052105,
			access_hash : 5933060422283347967,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 34,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'X1yrh4bfFpNVvYij',
					reason : 'Xh8FHU0y7Ozi9NLf',
					text : 'QMeSsPHzkaKrYxEG',
				),
			),
			bot_inline_placeholder : '2tA8lFo14f3jy5ZP',
			lang_code : 'ryT4OZa25vz0pECY',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 1,
			color : $client->peerColor(
				color : 84,
				background_emoji_id : -2135585216298894800,
			),
			profile_color : $client->peerColor(
				color : 80,
				background_emoji_id : 4751211122932536397,
			),
			bot_active_users : 24,
			bot_verification_icon : 5561988580542796389,
			send_paid_messages_stars : -2451704794457366872,
		),
	),
);
```