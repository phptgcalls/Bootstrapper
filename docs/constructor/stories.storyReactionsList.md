# stories.storyReactionsList

**Description** : *List of peers that reacted to or intercated with a specific story*

**Layer** : 211

```tl
stories.storyReactionsList#aa5f789c flags:# count:int reactions:Vector<StoryReaction> chats:Vector<Chat> users:Vector<User> next_offset:flags.0?string = stories.StoryReactionsList;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of reactions matching query |
| <mark>reactions</mark> | [`Vector<StoryReaction>`](type/StoryReaction) | List of peers that reacted to or interacted with a specific story |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |
| **next_offset** | [`flags.0?string`](type/string) | If set, indicates the next offset to use to load more results by invoking stories.getStoryReactionsList |

---

## Type

[stories.StoryReactionsList](type/stories.StoryReactionsList)

---

## Example

```php
$storiesStoryReactionsList = $client->stories->storyReactionsList(
	count : 77,
	reactions : array(
		$client->storyReaction(
			peer_id : $client->peerUser(
				user_id : -4552968658123580247,
			),
			date : 15,
			reaction : $client->reactionEmpty(),
		),
		$client->storyReactionPublicForward(
			message : $client->messageEmpty(
				id : 32,
				peer_id : $client->peerUser(...),
			),
		),
		$client->storyReactionPublicRepost(
			peer_id : $client->peerUser(
				user_id : -3281876902530286642,
			),
			story : $client->storyItemDeleted(
				id : 46,
			),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -6813408041016772488,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -772846685465024211,
			title : 'Ksyx4H2do3DSYTwh',
			photo : $client->chatPhotoEmpty(),
			participants_count : 55,
			date : 52,
			version : 80,
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
				until_date : 4,
			),
		),
		$client->chatForbidden(
			id : -8844613934186913451,
			title : 'TviFuRQ4mMqJ9Wyc',
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
			id : -396508137761229318,
			access_hash : 8557969142199098392,
			title : 'ObLpSfRD46NGTkeu',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 90,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'xbm9FPJZE18OcAeu',
					reason : 'MKDiVxAtd8fG7wYo',
					text : 'dGP4UDWOjr6Ce8M5',
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
				until_date : 83,
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
				until_date : 97,
			),
			participants_count : 21,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 13,
			color : $client->peerColor(
				color : 25,
				background_emoji_id : -4511370697735359928,
			),
			profile_color : $client->peerColor(
				color : 27,
				background_emoji_id : 3755493606259451638,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 68,
			subscription_until_date : 42,
			bot_verification_icon : -1875184367636373682,
			send_paid_messages_stars : 2683912819290099554,
			linked_monoforum_id : -7166264799353040945,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -9125474111599871408,
			access_hash : -8377042216372678525,
			title : '6BMJoyRAfQhPtclz',
			until_date : 53,
		),
	),
	users : array(
		$client->userEmpty(
			id : 2740319893115831607,
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
			id : 3366020943163947466,
			access_hash : 7462124132225405615,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 4,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'TWt5Xnsrkwg07lGa',
					reason : 'F5SU0vp6HoGfux7I',
					text : 'HFuDj8XCAq1N5feW',
				),
			),
			bot_inline_placeholder : 'zQTMp1Y0Fx6PoRCe',
			lang_code : 'QRAwCkoTz1Ubn2d7',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 43,
			color : $client->peerColor(
				color : 2,
				background_emoji_id : 2886226043407692330,
			),
			profile_color : $client->peerColor(
				color : 52,
				background_emoji_id : -6333014262592731317,
			),
			bot_active_users : 57,
			bot_verification_icon : 2938197589285412475,
			send_paid_messages_stars : 7060735476374980073,
		),
	),
	next_offset : 'UfbHclWMeEmKO0Nd',
);
```