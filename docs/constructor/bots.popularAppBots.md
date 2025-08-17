# bots.popularAppBots

**Description** : *Popular Main Mini Apps, to be used in the apps tab of global search »*

**Layer** : 211

```tl
bots.popularAppBots#1991b13b flags:# next_offset:flags.0?string users:Vector<User> = bots.PopularAppBots;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **next_offset** | [`flags.0?string`](type/string) | Offset for pagination |
| <mark>users</mark> | [`Vector<User>`](type/User) | The bots associated to each Main Mini App, see here » for more info |

---

## Type

[bots.PopularAppBots](type/bots.PopularAppBots)

---

## Example

```php
$botsPopularAppBots = $client->bots->popularAppBots(
	next_offset : '2feaPGUIzx3LD9ob',
	users : array(
		$client->userEmpty(
			id : 355751620593425280,
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
			id : -399955752917328045,
			access_hash : -4090599046506389500,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 59,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '6qJP5DxH4vnrcWIz',
					reason : 'QAx1V7SztGPdoZke',
					text : 'dYQHJWbAU2VLqhrT',
				),
			),
			bot_inline_placeholder : '9lV7WmSLgRQTAhCM',
			lang_code : 'qnQvbsz4cKZxoUdV',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 17,
			color : $client->peerColor(
				color : 67,
				background_emoji_id : -7745625178962657270,
			),
			profile_color : $client->peerColor(
				color : 58,
				background_emoji_id : 8113968728604991717,
			),
			bot_active_users : 83,
			bot_verification_icon : -4487870349121699873,
			send_paid_messages_stars : -1360202509961917067,
		),
	),
);
```