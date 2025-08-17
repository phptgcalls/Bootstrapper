# stories.foundStories

**Description** : *Stories found using global story search »*

**Layer** : 211

```tl
stories.foundStories#e2de7737 flags:# count:int stories:Vector<FoundStory> next_offset:flags.0?string chats:Vector<Chat> users:Vector<User> = stories.FoundStories;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of results found for the query |
| <mark>stories</mark> | [`Vector<FoundStory>`](type/FoundStory) | Matching stories |
| **next_offset** | [`flags.0?string`](type/string) | Offset used to fetch the next page, if not set this is the final page |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[stories.FoundStories](type/stories.FoundStories)

---

## Example

```php
$storiesFoundStories = $client->stories->foundStories(
	count : 33,
	stories : array(
		$client->foundStory(
			peer : $client->peerUser(
				user_id : -2286852125820022943,
			),
			story : $client->storyItemDeleted(
				id : 3,
			),
		),
	),
	next_offset : '2PESkKZ0Trz6sdVi',
	chats : array(
		$client->chatEmpty(
			id : -157342055434532974,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 3687967552921138569,
			title : '6iDUNGOSTB1PKsg7',
			photo : $client->chatPhotoEmpty(),
			participants_count : 39,
			date : 24,
			version : 27,
			migrated_to : $client->inputChannelEmpty(),
			admin_rights : $client->chatAdminRights(
				change_info : true,
				post_messages : true,
				edit_messages : true,
				delete_messages : true,
				ban_users : true,
				invite_users : true,
				pin_messages : true,
				add_admins : true,
				anonymous : true,
				manage_call : true,
				other : true,
				manage_topics : true,
				post_stories : true,
				edit_stories : true,
				delete_stories : true,
				manage_direct_messages : true,
			),
			default_banned_rights : $client->chatBannedRights(
				view_messages : true,
				send_messages : true,
				send_media : true,
				send_stickers : true,
				send_gifs : true,
				send_games : true,
				send_inline : true,
				embed_links : true,
				send_polls : true,
				change_info : true,
				invite_users : true,
				pin_messages : true,
				manage_topics : true,
				send_photos : true,
				send_videos : true,
				send_roundvideos : true,
				send_audios : true,
				send_voices : true,
				send_docs : true,
				send_plain : true,
				until_date : 55,
			),
		),
		$client->chatForbidden(
			id : 70651089352212324,
			title : 'Zp8z3yKouAIf7jcJ',
		),
		$client->channel(
			creator : true,
			left : true,
			broadcast : true,
			verified : true,
			megagroup : true,
			restricted : true,
			signatures : true,
			min : true,
			scam : true,
			has_link : true,
			has_geo : true,
			slowmode_enabled : true,
			call_active : true,
			call_not_empty : true,
			fake : true,
			gigagroup : true,
			noforwards : true,
			join_to_send : true,
			join_request : true,
			forum : true,
			stories_hidden : true,
			stories_hidden_min : true,
			stories_unavailable : true,
			signature_profiles : true,
			autotranslation : true,
			broadcast_messages_allowed : true,
			monoforum : true,
			forum_tabs : true,
			id : 1585087945011679112,
			access_hash : -1253129994321689219,
			title : '0o6E1lmOW5uKrGAp',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 55,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'tZvhynR0LIfTz4gr',
					reason : '1Ax3JrYcZGDsVTOP',
					text : 'qxgf3YbsMvaV0ck7',
				),
			),
			admin_rights : $client->chatAdminRights(
				change_info : true,
				post_messages : true,
				edit_messages : true,
				delete_messages : true,
				ban_users : true,
				invite_users : true,
				pin_messages : true,
				add_admins : true,
				anonymous : true,
				manage_call : true,
				other : true,
				manage_topics : true,
				post_stories : true,
				edit_stories : true,
				delete_stories : true,
				manage_direct_messages : true,
			),
			banned_rights : $client->chatBannedRights(
				view_messages : true,
				send_messages : true,
				send_media : true,
				send_stickers : true,
				send_gifs : true,
				send_games : true,
				send_inline : true,
				embed_links : true,
				send_polls : true,
				change_info : true,
				invite_users : true,
				pin_messages : true,
				manage_topics : true,
				send_photos : true,
				send_videos : true,
				send_roundvideos : true,
				send_audios : true,
				send_voices : true,
				send_docs : true,
				send_plain : true,
				until_date : 65,
			),
			default_banned_rights : $client->chatBannedRights(
				view_messages : true,
				send_messages : true,
				send_media : true,
				send_stickers : true,
				send_gifs : true,
				send_games : true,
				send_inline : true,
				embed_links : true,
				send_polls : true,
				change_info : true,
				invite_users : true,
				pin_messages : true,
				manage_topics : true,
				send_photos : true,
				send_videos : true,
				send_roundvideos : true,
				send_audios : true,
				send_voices : true,
				send_docs : true,
				send_plain : true,
				until_date : 46,
			),
			participants_count : 33,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 25,
			color : $client->peerColor(
				color : 83,
				background_emoji_id : -5446248442072492395,
			),
			profile_color : $client->peerColor(
				color : 85,
				background_emoji_id : -1170416420709345278,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 27,
			subscription_until_date : 30,
			bot_verification_icon : 795475875307274276,
			send_paid_messages_stars : -6216484838007197811,
			linked_monoforum_id : -2199236858841289242,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 2360751439412565261,
			access_hash : -2946330773627686057,
			title : 'DiBJSMyw1IOdh9qN',
			until_date : 45,
		),
	),
	users : array(
		$client->userEmpty(
			id : -6890976199711045313,
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
			id : -2264719885998100175,
			access_hash : 636473200224991173,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 56,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'J2EfgHRXvpULSkiQ',
					reason : 'ONjg1dEwoGcYP8ns',
					text : 'V7T3ovdO8LixqzAc',
				),
			),
			bot_inline_placeholder : '7pMwmkCKiGzOgByT',
			lang_code : 'CkRsTohVlnF7XGId',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 74,
			color : $client->peerColor(
				color : 14,
				background_emoji_id : -3130038435426583194,
			),
			profile_color : $client->peerColor(
				color : 5,
				background_emoji_id : 2646403371286970182,
			),
			bot_active_users : 40,
			bot_verification_icon : -4870956807465123053,
			send_paid_messages_stars : 3148957732002800845,
		),
	),
);
```