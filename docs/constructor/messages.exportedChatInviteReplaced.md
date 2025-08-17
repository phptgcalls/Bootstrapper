# messages.exportedChatInviteReplaced

**Description** : *The specified chat invite was replaced with another one*

**Layer** : 211

```tl
messages.exportedChatInviteReplaced#222600ef invite:ExportedChatInvite new_invite:ExportedChatInvite users:Vector<User> = messages.ExportedChatInvite;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | The replaced chat invite |
| <mark>new_invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | The invite that replaces the previous invite |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[messages.ExportedChatInvite](type/messages.ExportedChatInvite)

---

## Example

```php
$messagesExportedChatInvite = $client->messages->exportedChatInviteReplaced(
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'W8fHpduPkZ4O6JB1',
		admin_id : 2804076127291694778,
		date : 21,
		start_date : 2,
		expire_date : 24,
		usage_limit : 5,
		usage : 48,
		requested : 16,
		subscription_expired : 36,
		title : '5p2B47kbQYIzeosq',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 94,
			amount : 3528203588203625585,
		),
	),
	new_invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'Sna85psZUILqfGH2',
		admin_id : -8955561911386965844,
		date : 46,
		start_date : 51,
		expire_date : 47,
		usage_limit : 99,
		usage : 26,
		requested : 36,
		subscription_expired : 66,
		title : 'KYjuUx3gamFvhwJL',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 61,
			amount : -9089351249303983948,
		),
	),
	users : array(
		$client->userEmpty(
			id : -9015503527466308824,
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
			id : -7537152537663631231,
			access_hash : -958048495915392133,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 57,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'W3KBDuEZGSM4X59H',
					reason : 'tg3sX9Be86iJS2TA',
					text : 'QpexAbITmBg5li3k',
				),
			),
			bot_inline_placeholder : '8QX9HiN2aBIOPbZ5',
			lang_code : 'JbOdeWyT7BMX2UF3',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 92,
			color : $client->peerColor(
				color : 73,
				background_emoji_id : 653544063322511222,
			),
			profile_color : $client->peerColor(
				color : 77,
				background_emoji_id : 7487142032192740905,
			),
			bot_active_users : 9,
			bot_verification_icon : -4566197842799900285,
			send_paid_messages_stars : 4916957163100127242,
		),
	),
);
```