# photos.photo

**Description** : *Photo with auxiliary data*

**Layer** : 211

```tl
photos.photo#20212ca8 photo:Photo users:Vector<User> = photos.Photo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>photo</mark> | [`Photo`](type/Photo) | Photo |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users |

---

## Type

[photos.Photo](type/photos.Photo)

---

## Example

```php
$photosPhoto = $client->photos->photo(
	photo : $client->photoEmpty(
		id : 4812042599080096451,
	),
	users : array(
		$client->userEmpty(
			id : -6510327591209233543,
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
			id : 3558523887486304947,
			access_hash : -1835235402511687927,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 5,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Ue9onJNZQrwBkVMI',
					reason : '7jzqca52bv0dT6RX',
					text : 'FOg6slKJu5mZyWjr',
				),
			),
			bot_inline_placeholder : 'TwLlXVsFKH2ABNkP',
			lang_code : 'XeTFu7H4yJ5iAnlM',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 77,
			color : $client->peerColor(
				color : 83,
				background_emoji_id : -5916124473498753130,
			),
			profile_color : $client->peerColor(
				color : 68,
				background_emoji_id : -162490478923788190,
			),
			bot_active_users : 84,
			bot_verification_icon : 1334295511186466359,
			send_paid_messages_stars : 3375052135552641873,
		),
	),
);
```