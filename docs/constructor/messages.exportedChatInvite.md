# messages.exportedChatInvite

**Description** : *Info about a chat invite*

**Layer** : 211

```tl
messages.exportedChatInvite#1871be50 invite:ExportedChatInvite users:Vector<User> = messages.ExportedChatInvite;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | Info about the chat invite |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[messages.ExportedChatInvite](type/messages.ExportedChatInvite)

---

## Example

```php
$messagesExportedChatInvite = $client->messages->exportedChatInvite(
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'pNtJb5m6S2iLlQYy',
		admin_id : -5663893351847796587,
		date : 51,
		start_date : 45,
		expire_date : 5,
		usage_limit : 87,
		usage : 97,
		requested : 29,
		subscription_expired : 7,
		title : 'FUTaI50syB37qVuN',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 47,
			amount : 5428726527747345600,
		),
	),
	users : array(
		$client->userEmpty(
			id : 7872755103915019764,
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
			id : 2874462764598200331,
			access_hash : 2058048836868152824,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 56,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '31jbL2wvRVrphSnM',
					reason : 'PkH0bB8ZYNUyrWaG',
					text : 'yZjnT1bFUhDivBJG',
				),
			),
			bot_inline_placeholder : 'VsTnaOZ9AfH2FK8p',
			lang_code : 'gmvzklxFIbDQyR5p',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 5,
			color : $client->peerColor(
				color : 69,
				background_emoji_id : -2333040656513166139,
			),
			profile_color : $client->peerColor(
				color : 6,
				background_emoji_id : -7518267916709281920,
			),
			bot_active_users : 10,
			bot_verification_icon : -1370885220015619637,
			send_paid_messages_stars : -6135636089253577968,
		),
	),
);
```