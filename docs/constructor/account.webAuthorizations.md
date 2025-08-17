# account.webAuthorizations

**Description** : *Web authorizations*

**Layer** : 211

```tl
account.webAuthorizations#ed56c9fc authorizations:Vector<WebAuthorization> users:Vector<User> = account.WebAuthorizations;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>authorizations</mark> | [`Vector<WebAuthorization>`](type/WebAuthorization) | Web authorization list |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users |

---

## Type

[account.WebAuthorizations](type/account.WebAuthorizations)

---

## Example

```php
$accountWebAuthorizations = $client->account->webAuthorizations(
	authorizations : array(
		$client->webAuthorization(
			hash : -9027247559200800927,
			bot_id : -9100527960089552981,
			domain : 'BsnfzUKN4eb6j1Go',
			browser : 'cwaHjICo9iLvY75g',
			platform : 'ilzVZ4os1f7nEjUc',
			date_created : 83,
			date_active : 18,
			ip : '127.0.0.1',
			region : 'oQfNSYD1ctq8yMzn',
		),
	),
	users : array(
		$client->userEmpty(
			id : -3433594036866345362,
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
			id : 5917454499079116848,
			access_hash : 1572543944012482361,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 5,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'mhXGvlnDzy9WqIkH',
					reason : 'm4F2bSgjHVRoI3dA',
					text : 'LiW453DuHwbydk8X',
				),
			),
			bot_inline_placeholder : 'jZJdh4zWM5nveacm',
			lang_code : 'p8HVh3Niljm9gf2e',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 54,
			color : $client->peerColor(
				color : 85,
				background_emoji_id : -7741198379128864080,
			),
			profile_color : $client->peerColor(
				color : 70,
				background_emoji_id : 1699165332916431015,
			),
			bot_active_users : 2,
			bot_verification_icon : 1151418093195703780,
			send_paid_messages_stars : -2194266015393064592,
		),
	),
);
```