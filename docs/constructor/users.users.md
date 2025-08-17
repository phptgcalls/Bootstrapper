# users.users

**Layer** : 211

```tl
users.users#62d706b8 users:Vector<User> = users.Users;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>users</mark> | [`Vector<User>`](type/User) | NOTHING |

---

## Type

[users.Users](type/users.Users)

---

## Example

```php
$usersUsers = $client->users->users(
	users : array(
		$client->userEmpty(
			id : -567154731061784483,
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
			id : -836918259841689864,
			access_hash : -4177675539711743398,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 24,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '6Fyj58wvsMJexlLp',
					reason : 'afhEpC07Jd2IKlqi',
					text : 'a9v5oYeIbs8fgRwX',
				),
			),
			bot_inline_placeholder : 'fwl5EoZ0erTqIPFa',
			lang_code : 'YNDxoTl6EyAZFPgi',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 44,
			color : $client->peerColor(
				color : 47,
				background_emoji_id : 329518285318007022,
			),
			profile_color : $client->peerColor(
				color : 1,
				background_emoji_id : 3863925642631455234,
			),
			bot_active_users : 55,
			bot_verification_icon : 1046630900010437775,
			send_paid_messages_stars : -8426625917803467994,
		),
	),
);
```