# messages.webPagePreview

**Layer** : 211

```tl
messages.webPagePreview#b53e8b21 media:MessageMedia users:Vector<User> = messages.WebPagePreview;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>media</mark> | [`MessageMedia`](type/MessageMedia) | NOTHING |
| <mark>users</mark> | [`Vector<User>`](type/User) | NOTHING |

---

## Type

[messages.WebPagePreview](type/messages.WebPagePreview)

---

## Example

```php
$messagesWebPagePreview = $client->messages->webPagePreview(
	media : $client->messageMediaEmpty(),
	users : array(
		$client->userEmpty(
			id : -2586362159031153419,
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
			id : 1240270045456746104,
			access_hash : 414202083135998430,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 72,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '1RJZelvQG0pdtn6E',
					reason : 'LauNHeA2bvoMKd6Q',
					text : '8PvazsrIVSOR4MLb',
				),
			),
			bot_inline_placeholder : 'tHmczpFs4G32L5J9',
			lang_code : 'mJuMTthgrE4c7ePD',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 90,
			color : $client->peerColor(
				color : 3,
				background_emoji_id : -3203529089141034411,
			),
			profile_color : $client->peerColor(
				color : 1,
				background_emoji_id : -7144476691889706873,
			),
			bot_active_users : 74,
			bot_verification_icon : -5928194579348585480,
			send_paid_messages_stars : -8837102343387710510,
		),
	),
);
```