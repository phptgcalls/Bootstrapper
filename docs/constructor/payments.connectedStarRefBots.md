# payments.connectedStarRefBots

**Description** : *Active affiliations*

**Layer** : 211

```tl
payments.connectedStarRefBots#98d5ea1d count:int connected_bots:Vector<ConnectedBotStarRef> users:Vector<User> = payments.ConnectedStarRefBots;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Total number of active affiliations |
| <mark>connected_bots</mark> | [`Vector<ConnectedBotStarRef>`](type/ConnectedBotStarRef) | The affiliations |
| <mark>users</mark> | [`Vector<User>`](type/User) | Peers mentioned in connected_bots |

---

## Type

[payments.ConnectedStarRefBots](type/payments.ConnectedStarRefBots)

---

## Example

```php
$paymentsConnectedStarRefBots = $client->payments->connectedStarRefBots(
	count : 35,
	connected_bots : array(
		$client->connectedBotStarRef(
			revoked : true,
			url : 'https://docs.liveproto.dev',
			date : 14,
			bot_id : 3658245179370836145,
			commission_permille : 5,
			duration_months : 44,
			participants : -3405572696112570662,
			revenue : 5839061986052226625,
		),
	),
	users : array(
		$client->userEmpty(
			id : -8134014491155748342,
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
			id : 4175847343176331485,
			access_hash : -6447866232928893773,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 32,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '1IbC9Z4haym5gQlu',
					reason : 'IBh6OKjDVZiXuFU1',
					text : 'bnPqwce2STomlGfr',
				),
			),
			bot_inline_placeholder : 'EUKylaw7CZT8tpcn',
			lang_code : 'e7vpgYTXIGnFfr40',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 35,
			color : $client->peerColor(
				color : 72,
				background_emoji_id : 1140169486593833753,
			),
			profile_color : $client->peerColor(
				color : 65,
				background_emoji_id : 2494874491177840148,
			),
			bot_active_users : 55,
			bot_verification_icon : -8016918855853518890,
			send_paid_messages_stars : -7718396676525323023,
		),
	),
);
```