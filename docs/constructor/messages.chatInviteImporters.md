# messages.chatInviteImporters

**Description** : *Info about the users that joined the chat using a specific chat invite*

**Layer** : 211

```tl
messages.chatInviteImporters#81b6b00a count:int importers:Vector<ChatInviteImporter> users:Vector<User> = messages.ChatInviteImporters;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Number of users that joined |
| <mark>importers</mark> | [`Vector<ChatInviteImporter>`](type/ChatInviteImporter) | The users that joined |
| <mark>users</mark> | [`Vector<User>`](type/User) | The users that joined |

---

## Type

[messages.ChatInviteImporters](type/messages.ChatInviteImporters)

---

## Example

```php
$messagesChatInviteImporters = $client->messages->chatInviteImporters(
	count : 73,
	importers : array(
		$client->chatInviteImporter(
			requested : true,
			via_chatlist : true,
			user_id : -1310818003759825342,
			date : 49,
			about : 'M0GiyzIq9C5DvnfF',
			approved_by : -6218926945911784787,
		),
	),
	users : array(
		$client->userEmpty(
			id : 1517559074911643966,
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
			id : -7448586773473688547,
			access_hash : -4209361192152705273,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 63,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'KEScRVo2ux1aLstd',
					reason : 'tmUdrF3ngEO1bchJ',
					text : '36czFhpGrkTx1RKC',
				),
			),
			bot_inline_placeholder : 'w0QyAJaM3BE5W6xZ',
			lang_code : 'tZAU2aqRnufVYm7i',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 14,
			color : $client->peerColor(
				color : 77,
				background_emoji_id : -1994065955311567981,
			),
			profile_color : $client->peerColor(
				color : 35,
				background_emoji_id : 8622925571252262111,
			),
			bot_active_users : 45,
			bot_verification_icon : 7033264100593926790,
			send_paid_messages_stars : -6076501313088146071,
		),
	),
);
```