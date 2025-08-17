# contacts.contactBirthdays

**Description** : *Birthday information of our contacts*

**Layer** : 211

```tl
contacts.contactBirthdays#114ff30d contacts:Vector<ContactBirthday> users:Vector<User> = contacts.ContactBirthdays;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>contacts</mark> | [`Vector<ContactBirthday>`](type/ContactBirthday) | Birthday info |
| <mark>users</mark> | [`Vector<User>`](type/User) | User information |

---

## Type

[contacts.ContactBirthdays](type/contacts.ContactBirthdays)

---

## Example

```php
$contactsContactBirthdays = $client->contacts->contactBirthdays(
	contacts : array(
		$client->contactBirthday(
			contact_id : 5425071170911334089,
			birthday : $client->birthday(
				day : 93,
				month : 4,
				year : 2,
			),
		),
	),
	users : array(
		$client->userEmpty(
			id : -5495036269364901292,
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
			id : -1081823177584849763,
			access_hash : -7634257161147849360,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 65,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'ShpJ90cWo72E85VL',
					reason : 'fJkZwDguTM7tH9Uz',
					text : 'StpbU8a5NC0Twv3Q',
				),
			),
			bot_inline_placeholder : 'qOjBbJV98oS6FW2s',
			lang_code : 'fvTxGNtkw3Qmrqy5',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 66,
			color : $client->peerColor(
				color : 58,
				background_emoji_id : -4332571706624632384,
			),
			profile_color : $client->peerColor(
				color : 7,
				background_emoji_id : -2402372043018982507,
			),
			bot_active_users : 21,
			bot_verification_icon : -5500790670195964627,
			send_paid_messages_stars : -8759451638647716187,
		),
	),
);
```