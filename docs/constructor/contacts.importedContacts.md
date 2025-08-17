# contacts.importedContacts

**Description** : *Info on successfully imported contacts*

**Layer** : 211

```tl
contacts.importedContacts#77d01c3b imported:Vector<ImportedContact> popular_invites:Vector<PopularContact> retry_contacts:Vector<long> users:Vector<User> = contacts.ImportedContacts;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>imported</mark> | [`Vector<ImportedContact>`](type/ImportedContact) | List of successfully imported contacts |
| <mark>popular_invites</mark> | [`Vector<PopularContact>`](type/PopularContact) | Popular contacts |
| <mark>retry_contacts</mark> | [`Vector<long>`](type/long) | List of contact ids that could not be imported due to system limitation and will need to be imported at a later date |
| <mark>users</mark> | [`Vector<User>`](type/User) | List of users |

---

## Type

[contacts.ImportedContacts](type/contacts.ImportedContacts)

---

## Example

```php
$contactsImportedContacts = $client->contacts->importedContacts(
	imported : array(
		$client->importedContact(
			user_id : -4092565740859488115,
			client_id : -6869878686088281540,
		),
	),
	popular_invites : array(
		$client->popularContact(
			client_id : 2369830121965287195,
			importers : 6,
		),
	),
	retry_contacts : array(-310577700391123995),
	users : array(
		$client->userEmpty(
			id : -8474215185292010894,
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
			id : -5349738415394654893,
			access_hash : 1709015118050236327,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 100,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'cPmqpebEwGX5jSvV',
					reason : 'S3ylvoNEieTMb6p9',
					text : '8bLxvHmV90XEW6r7',
				),
			),
			bot_inline_placeholder : 'S7Zt3LDAeTPkbhgG',
			lang_code : 'PywrWTXcUFuiL2q9',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 67,
			color : $client->peerColor(
				color : 41,
				background_emoji_id : -2749315420139090499,
			),
			profile_color : $client->peerColor(
				color : 68,
				background_emoji_id : 6977294024470190341,
			),
			bot_active_users : 61,
			bot_verification_icon : 2942947790053957502,
			send_paid_messages_stars : -4739513441832695636,
		),
	),
);
```