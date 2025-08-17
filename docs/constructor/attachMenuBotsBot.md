# attachMenuBotsBot

**Description** : *Represents a bot mini app that can be launched from the attachment menu »*

**Layer** : 211

```tl
attachMenuBotsBot#93bf667f bot:AttachMenuBot users:Vector<User> = AttachMenuBotsBot;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>bot</mark> | [`AttachMenuBot`](type/AttachMenuBot) | Represents a bot mini app that can be launched from the attachment menu » |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about related users and bots |

---

## Type

[AttachMenuBotsBot](type/AttachMenuBotsBot)

---

## Example

```php
$attachMenuBotsBot = $client->attachMenuBotsBot(
	bot : $client->attachMenuBot(
		inactive : true,
		has_settings : true,
		request_write_access : true,
		show_in_attach_menu : true,
		show_in_side_menu : true,
		side_menu_disclaimer_needed : true,
		bot_id : 6308644931393748176,
		short_name : 'ImsyBGc0R9fwbFaC',
		peer_types : array(
			$client->attachMenuPeerTypeSameBotPM(),
			$client->attachMenuPeerTypeBotPM(),
			$client->attachMenuPeerTypePM(),
			$client->attachMenuPeerTypeChat(),
			$client->attachMenuPeerTypeBroadcast(),
		),
		icons : array(
			$client->attachMenuBotIcon(
				name : '0i9zPlGvrEoaWR5B',
				icon : $client->documentEmpty(...),
				colors : array(
					$client->attachMenuBotIconColor(...),
				),
			),
		),
	),
	users : array(
		$client->userEmpty(
			id : -5270106237707427246,
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
			id : -5414661618917782469,
			access_hash : -386575188119454174,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 19,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'MTm2yrIs6igxpHA4',
					reason : 'CYqn9Dd4i5Ntyrho',
					text : 'PruMjQLs3z7vFqUS',
				),
			),
			bot_inline_placeholder : 'fPKzDxhGTXLstiWy',
			lang_code : 'Tj76vXtE2oeSqfQk',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 69,
			color : $client->peerColor(
				color : 52,
				background_emoji_id : -681186268517337965,
			),
			profile_color : $client->peerColor(
				color : 22,
				background_emoji_id : 7043563580374747316,
			),
			bot_active_users : 82,
			bot_verification_icon : -3545690675817509708,
			send_paid_messages_stars : 704569645693879098,
		),
	),
);
```