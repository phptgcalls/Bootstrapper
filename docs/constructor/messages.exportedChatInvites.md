# messages.exportedChatInvites

**Description** : *Info about chat invites exported by a certain admin*

**Layer** : 211

```tl
messages.exportedChatInvites#bdc62dcc count:int invites:Vector<ExportedChatInvite> users:Vector<User> = messages.ExportedChatInvites;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>count</mark> | [`int`](type/int) | Number of invites exported by the admin |
| <mark>invites</mark> | [`Vector<ExportedChatInvite>`](type/ExportedChatInvite) | Exported invites |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about the admin |

---

## Type

[messages.ExportedChatInvites](type/messages.ExportedChatInvites)

---

## Example

```php
$messagesExportedChatInvites = $client->messages->exportedChatInvites(
	count : 39,
	invites : array(
		$client->chatInviteExported(
			revoked : true,
			permanent : true,
			request_needed : true,
			link : '0EnjQwJxIprPAGLd',
			admin_id : 573456495280160320,
			date : 39,
			start_date : 53,
			expire_date : 16,
			usage_limit : 62,
			usage : 20,
			requested : 45,
			subscription_expired : 69,
			title : 'y5ICjrBp9VflW1HE',
			subscription_pricing : $client->starsSubscriptionPricing(
				period : 50,
				amount : -1013257437204926056,
			),
		),
		$client->chatInvitePublicJoinRequests(),
	),
	users : array(
		$client->userEmpty(
			id : 4478512859320167371,
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
			id : -2409570581150501011,
			access_hash : 3126940049714608567,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 68,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'dset0oM8uHalpmJW',
					reason : 'cb84WsdVwMFjhSxn',
					text : 'AioMkIUrHvDOm30S',
				),
			),
			bot_inline_placeholder : 'IfzBaUuboed7Wcxk',
			lang_code : 'yrTJb02vqlU5zt8F',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 17,
			color : $client->peerColor(
				color : 29,
				background_emoji_id : -5164806748003420192,
			),
			profile_color : $client->peerColor(
				color : 76,
				background_emoji_id : 6304051163985709654,
			),
			bot_active_users : 40,
			bot_verification_icon : -8275766733622334401,
			send_paid_messages_stars : -2454671143871622593,
		),
	),
);
```