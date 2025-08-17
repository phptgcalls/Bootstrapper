# phone.phoneCall

**Description** : *A VoIP phone call*

**Layer** : 211

```tl
phone.phoneCall#ec82e140 phone_call:PhoneCall users:Vector<User> = phone.PhoneCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>phone_call</mark> | [`PhoneCall`](type/PhoneCall) | The VoIP phone call |
| <mark>users</mark> | [`Vector<User>`](type/User) | VoIP phone call participants |

---

## Type

[phone.PhoneCall](type/phone.PhoneCall)

---

## Example

```php
$phonePhoneCall = $client->phone->phoneCall(
	phone_call : $client->phoneCallEmpty(
		id : -6714381896171914827,
	),
	users : array(
		$client->userEmpty(
			id : 4258312227903038826,
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
			id : -7543549757736481757,
			access_hash : 1563149921882008361,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 89,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '6PAHNDmanJj2Tyit',
					reason : 'RjHk0f6E3MrLlAIt',
					text : 'w5qsfKlTUthVSgdv',
				),
			),
			bot_inline_placeholder : '1cwtGWbKE3msk8Iv',
			lang_code : 'U6lymqSxrtBjOKcd',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 31,
			color : $client->peerColor(
				color : 88,
				background_emoji_id : -7403264751471191068,
			),
			profile_color : $client->peerColor(
				color : 65,
				background_emoji_id : 1984409367276545751,
			),
			bot_active_users : 69,
			bot_verification_icon : 177158884834568855,
			send_paid_messages_stars : -7397693773521107753,
		),
	),
);
```