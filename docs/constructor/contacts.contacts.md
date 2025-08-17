# contacts.contacts

**Description** : *The current user's contact list and info on users*

**Layer** : 211

```tl
contacts.contacts#eae87e42 contacts:Vector<Contact> saved_count:int users:Vector<User> = contacts.Contacts;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>contacts</mark> | [`Vector<Contact>`](type/Contact) | Contact list |
| <mark>saved_count</mark> | [`int`](type/int) | Number of contacts that were saved successfully |
| <mark>users</mark> | [`Vector<User>`](type/User) | User list |

---

## Type

[contacts.Contacts](type/contacts.Contacts)

---

## Example

```php
$contactsContacts = $client->contacts->contacts(
	contacts : array(
		$client->contact(
			user_id : 2904833270683447691,
			mutual : $client->boolFalse(),
		),
	),
	saved_count : 13,
	users : array(
		$client->userEmpty(
			id : 1574552371574285199,
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
			id : -8725498412413349319,
			access_hash : 7772198736423688349,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 95,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'EXiG3oVTBc10Rxa8',
					reason : 'DQUakG0eRK79BEI3',
					text : 'ePVM9i4nva2Hogrj',
				),
			),
			bot_inline_placeholder : '8locsU2KvCpgkSZf',
			lang_code : 'oaDOpkludgeiFTCY',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 51,
			color : $client->peerColor(
				color : 70,
				background_emoji_id : -2638359912120844977,
			),
			profile_color : $client->peerColor(
				color : 93,
				background_emoji_id : -3349979758446818625,
			),
			bot_active_users : 76,
			bot_verification_icon : 8117373528009780473,
			send_paid_messages_stars : -4469949036091810138,
		),
	),
);
```