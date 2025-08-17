# account.connectedBots

**Description** : *Info about currently connected business bots*

**Layer** : 211

```tl
account.connectedBots#17d7f87b connected_bots:Vector<ConnectedBot> users:Vector<User> = account.ConnectedBots;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>connected_bots</mark> | [`Vector<ConnectedBot>`](type/ConnectedBot) | Info about the connected bots |
| <mark>users</mark> | [`Vector<User>`](type/User) | Bot information |

---

## Type

[account.ConnectedBots](type/account.ConnectedBots)

---

## Example

```php
$accountConnectedBots = $client->account->connectedBots(
	connected_bots : array(
		$client->connectedBot(
			bot_id : -8527766039634627191,
			recipients : $client->businessBotRecipients(
				existing_chats : true,
				new_chats : true,
				contacts : true,
				non_contacts : true,
				exclude_selected : true,
				users : array(9191625117396648292),
				exclude_users : array(-4504466693292070802),
			),
			rights : $client->businessBotRights(
				reply : true,
				read_messages : true,
				delete_sent_messages : true,
				delete_received_messages : true,
				edit_name : true,
				edit_bio : true,
				edit_profile_photo : true,
				edit_username : true,
				view_gifts : true,
				sell_gifts : true,
				change_gift_settings : true,
				transfer_and_upgrade_gifts : true,
				transfer_stars : true,
				manage_stories : true,
			),
		),
	),
	users : array(
		$client->userEmpty(
			id : -4181602328650630582,
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
			id : 8357500364846053578,
			access_hash : 6608315168467779111,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 63,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '2BAqycvSVagQfFil',
					reason : 'Jqf94FYGcP6hS3UC',
					text : '0kLsy8gNWpxPv74f',
				),
			),
			bot_inline_placeholder : 'XsDBg2dRt5Z1fTh8',
			lang_code : 'FwrQ8tcHfOUi0esW',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 53,
			color : $client->peerColor(
				color : 90,
				background_emoji_id : 78619279734545159,
			),
			profile_color : $client->peerColor(
				color : 87,
				background_emoji_id : -2018147108969494909,
			),
			bot_active_users : 68,
			bot_verification_icon : -2613565080804671267,
			send_paid_messages_stars : 1336572544303251421,
		),
	),
);
```