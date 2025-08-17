# messages.highScores

**Description** : *Highscores in a game*

**Layer** : 211

```tl
messages.highScores#9a3bfd99 scores:Vector<HighScore> users:Vector<User> = messages.HighScores;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>scores</mark> | [`Vector<HighScore>`](type/HighScore) | Highscores |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users, associated to the highscores |

---

## Type

[messages.HighScores](type/messages.HighScores)

---

## Example

```php
$messagesHighScores = $client->messages->highScores(
	scores : array(
		$client->highScore(
			pos : 89,
			user_id : 749939715112935020,
			score : 20,
		),
	),
	users : array(
		$client->userEmpty(
			id : -5389727180113877337,
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
			id : 8625130308887852642,
			access_hash : 6825219308873131220,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 98,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'zv1N3fSCx2TJyGrQ',
					reason : 'CJLlXYRF5n9NjK7T',
					text : 'mGVQarO9TJ1MdH0D',
				),
			),
			bot_inline_placeholder : 'AUDrPTaXgbsLZ3l2',
			lang_code : 'Zu7P3yDnkjz2pKds',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 43,
			color : $client->peerColor(
				color : 41,
				background_emoji_id : 2120327794090375045,
			),
			profile_color : $client->peerColor(
				color : 82,
				background_emoji_id : -2099813133692345431,
			),
			bot_active_users : 7,
			bot_verification_icon : 833313189148058493,
			send_paid_messages_stars : 4010704546377239264,
		),
	),
);
```