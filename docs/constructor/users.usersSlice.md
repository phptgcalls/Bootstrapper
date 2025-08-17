# users.usersSlice

**Layer** : 211

```tl
users.usersSlice#315a4974 count:int users:Vector<User> = users.Users;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | NOTHING |
| <mark>users</mark> | [`Vector<User>`](type/User) | NOTHING |

---

## Type

[users.Users](type/users.Users)

---

## Example

```php
$usersUsers = $client->users->usersSlice(
	count : 65,
	users : array(
		$client->userEmpty(
			id : 6733401658663936493,
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
			id : 603593428163984754,
			access_hash : -477391774437322565,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 72,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'ChG0vAXipw1s4zfN',
					reason : 'XQrWdRGqJN0twsZ1',
					text : 'KuE6dlUS1TQvPbk0',
				),
			),
			bot_inline_placeholder : 'oXRAWnSYsv2qOz8I',
			lang_code : 'FEJksv71U4xdzAji',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 38,
			color : $client->peerColor(
				color : 23,
				background_emoji_id : -1983599195937795178,
			),
			profile_color : $client->peerColor(
				color : 81,
				background_emoji_id : -8709351261504364766,
			),
			bot_active_users : 36,
			bot_verification_icon : -2247729463690414246,
			send_paid_messages_stars : -4856179287758532212,
		),
	),
);
```