# premium.boostsList

**Description** : *List of boosts that were applied to a peer by multiple users*

**Layer** : 211

```tl
premium.boostsList#86f8613c flags:# count:int boosts:Vector<Boost> next_offset:flags.0?string users:Vector<User> = premium.BoostsList;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of results |
| <mark>boosts</mark> | [`Vector<Boost>`](type/Boost) | Boosts |
| **next_offset** | [`flags.0?string`](type/string) | Offset that can be used for pagination |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[premium.BoostsList](type/premium.BoostsList)

---

## Example

```php
$premiumBoostsList = $client->premium->boostsList(
	count : 56,
	boosts : array(
		$client->boost(
			gift : true,
			giveaway : true,
			unclaimed : true,
			id : 'uVHlCUawjQRmY9NB',
			user_id : 6339254877959389552,
			giveaway_msg_id : 70,
			date : 42,
			expires : 56,
			used_gift_slug : '2DmMF0nxJjiB4TuQ',
			multiplier : 1,
			stars : 5217984989996103508,
		),
	),
	next_offset : 'dFSmQWhAIzY5ZXLn',
	users : array(
		$client->userEmpty(
			id : 3875679039125836055,
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
			id : 1517105248985153451,
			access_hash : 5339344266062663682,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 1,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '5zT2ajKkQEn1UxlF',
					reason : 'cfolnywzRjX93reE',
					text : 'juQMOmzKtso5lCV3',
				),
			),
			bot_inline_placeholder : 'bdngR3J4qEZ8CQKu',
			lang_code : 'TRGHJkbLXNmV02h6',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 12,
			color : $client->peerColor(
				color : 8,
				background_emoji_id : 8986490003026044399,
			),
			profile_color : $client->peerColor(
				color : 96,
				background_emoji_id : 8244369523012780977,
			),
			bot_active_users : 16,
			bot_verification_icon : 3342464208047098154,
			send_paid_messages_stars : 3684021687065993950,
		),
	),
);
```