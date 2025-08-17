# payments.suggestedStarRefBots

**Description** : *A list of suggested mini apps with available affiliate programs*

**Layer** : 211

```tl
payments.suggestedStarRefBots#b4d5d859 flags:# count:int suggested_bots:Vector<StarRefProgram> users:Vector<User> next_offset:flags.0?string = payments.SuggestedStarRefBots;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of results (for pagination) |
| <mark>suggested_bots</mark> | [`Vector<StarRefProgram>`](type/StarRefProgram) | Suggested affiliate programs (full or partial list to be fetched using pagination) |
| <mark>users</mark> | [`Vector<User>`](type/User) | Peers mentioned in suggested_bots |
| **next_offset** | [`flags.0?string`](type/string) | Next offset for pagination |

---

## Type

[payments.SuggestedStarRefBots](type/payments.SuggestedStarRefBots)

---

## Example

```php
$paymentsSuggestedStarRefBots = $client->payments->suggestedStarRefBots(
	count : 12,
	suggested_bots : array(
		$client->starRefProgram(
			bot_id : -5887556463615824882,
			commission_permille : 21,
			duration_months : 47,
			end_date : 7,
			daily_revenue_per_user : $client->starsAmount(
				amount : 5053188702171165267,
				nanos : 38,
			),
		),
	),
	users : array(
		$client->userEmpty(
			id : 2890427367342871327,
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
			id : 7062977313041217230,
			access_hash : -8934727722254028096,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 98,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '04Y2KrD9L7QgUTVC',
					reason : 'D3w9qfr71hCzO8md',
					text : 'qJ8me1roVxsgHU0u',
				),
			),
			bot_inline_placeholder : 'OuS5YFmNjIfxAyVp',
			lang_code : 'meyqcxYbOhfoFTju',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 84,
			color : $client->peerColor(
				color : 6,
				background_emoji_id : -3396031926426275346,
			),
			profile_color : $client->peerColor(
				color : 24,
				background_emoji_id : 7059138980621644853,
			),
			bot_active_users : 89,
			bot_verification_icon : -2032326405134046916,
			send_paid_messages_stars : 9064963572549963541,
		),
	),
	next_offset : 'NMbofFkGVRpuSx05',
);
```