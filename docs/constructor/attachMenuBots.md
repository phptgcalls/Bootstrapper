# attachMenuBots

**Description** : *Represents a list of bot mini apps that can be launched from the attachment menu »*

**Layer** : 211

```tl
attachMenuBots#3c4301c0 hash:long bots:Vector<AttachMenuBot> users:Vector<User> = AttachMenuBots;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>bots</mark> | [`Vector<AttachMenuBot>`](type/AttachMenuBot) | List of bot mini apps that can be launched from the attachment menu » |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about related users/bots |

---

## Type

[AttachMenuBots](type/AttachMenuBots)

---

## Example

```php
$attachMenuBots = $client->attachMenuBots(
	hash : -4787164746311354809,
	bots : array(
		$client->attachMenuBot(
			inactive : true,
			has_settings : true,
			request_write_access : true,
			show_in_attach_menu : true,
			show_in_side_menu : true,
			side_menu_disclaimer_needed : true,
			bot_id : 48618487070472238,
			short_name : 'bg3RifKhFGc429s5',
			peer_types : array(
				$client->attachMenuPeerTypeSameBotPM(),
				$client->attachMenuPeerTypeBotPM(),
				$client->attachMenuPeerTypePM(),
				$client->attachMenuPeerTypeChat(),
				$client->attachMenuPeerTypeBroadcast(),
			),
			icons : array(
				$client->attachMenuBotIcon(
					name : 'TDxGsvV3phtJAN7b',
					icon : $client->documentEmpty(...),
					colors : array(
						$client->attachMenuBotIconColor(...),
					),
				),
			),
		),
	),
	users : array(
		$client->userEmpty(
			id : -1812471951479714109,
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
			id : -1816063352946637633,
			access_hash : 1512882472269452886,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 98,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'mXnVQd3kMebNsWh7',
					reason : 'HbUIMgydpZDshRXW',
					text : 'AkcpX4RPqFz2B3x0',
				),
			),
			bot_inline_placeholder : 'HM2k5ERrC8UzelWu',
			lang_code : 'msnDVu41GdxwXcya',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 50,
			color : $client->peerColor(
				color : 94,
				background_emoji_id : -8555560257104032248,
			),
			profile_color : $client->peerColor(
				color : 1,
				background_emoji_id : 383720421530614072,
			),
			bot_active_users : 31,
			bot_verification_icon : -8776377997443137382,
			send_paid_messages_stars : -3067631553831782986,
		),
	),
);
```