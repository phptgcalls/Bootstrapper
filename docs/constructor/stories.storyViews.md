# stories.storyViews

**Description** : *Reaction and view counters for a list of stories*

**Layer** : 211

```tl
stories.storyViews#de9eed1d views:Vector<StoryViews> users:Vector<User> = stories.StoryViews;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>views</mark> | [`Vector<StoryViews>`](type/StoryViews) | View date and reaction information of multiple stories |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |

---

## Type

[stories.StoryViews](type/stories.StoryViews)

---

## Example

```php
$storiesStoryViews = $client->stories->storyViews(
	views : array(
		$client->storyViews(
			has_viewers : true,
			views_count : 86,
			forwards_count : 77,
			reactions : array(
				$client->reactionCount(
					chosen_order : 28,
					reaction : $client->reactionEmpty(...),
					count : 30,
				),
			),
			reactions_count : 56,
			recent_viewers : array(7194014988702474543),
		),
	),
	users : array(
		$client->userEmpty(
			id : 738999155624200185,
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
			id : -6618450985708694240,
			access_hash : -2809253388102651615,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 17,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'gcvJPV3ea4pT2kMA',
					reason : 'jyhAdCxriNblo2IM',
					text : 'MbCFlr6Ux9eDq8SH',
				),
			),
			bot_inline_placeholder : 'yiGXWAC8qD9eoSdv',
			lang_code : 'eF0jr43c5lpvuoL7',
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
				color : 44,
				background_emoji_id : 2097062287573394498,
			),
			profile_color : $client->peerColor(
				color : 4,
				background_emoji_id : 1538856029077573212,
			),
			bot_active_users : 44,
			bot_verification_icon : -146149478271053270,
			send_paid_messages_stars : -7406166376705720236,
		),
	),
);
```