# messages.messageReactionsList

**Description** : *List of peers that reacted to a specific message*

**Layer** : 211

```tl
messages.messageReactionsList#31bd492d flags:# count:int reactions:Vector<MessagePeerReaction> chats:Vector<Chat> users:Vector<User> next_offset:flags.0?string = messages.MessageReactionsList;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of reactions matching query |
| <mark>reactions</mark> | [`Vector<MessagePeerReaction>`](type/MessagePeerReaction) | List of peers that reacted to a specific message |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Mentioned users |
| **next_offset** | [`flags.0?string`](type/string) | If set, indicates the next offset to use to load more results by invoking messages.getMessageReactionsList |

---

## Type

[messages.MessageReactionsList](type/messages.MessageReactionsList)

---

## Example

```php
$messagesMessageReactionsList = $client->messages->messageReactionsList(
	count : 3,
	reactions : array(
		$client->messagePeerReaction(
			big : true,
			unread : true,
			my : true,
			peer_id : $client->peerUser(
				user_id : -7988597020348899774,
			),
			date : 15,
			reaction : $client->reactionEmpty(),
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -7131088332603298604,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 5269823869109756168,
			title : '5a9gR4XCqs8hmdxy',
			photo : $client->chatPhotoEmpty(),
			participants_count : 11,
			date : 70,
			version : 2,
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
				until_date : 26,
			),
		),
		$client->chatForbidden(
			id : 5953405853423554359,
			title : 'rDc31KSmqTwb5QkE',
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
			id : 629735627642683580,
			access_hash : -1182153471753703512,
			title : 'h6cFrs7JvleTRPNZ',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 44,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'j1wpqcILA2tErUdb',
					reason : 'WvygQpUj4D365G8i',
					text : 'YNszPuvV4ex6IKm2',
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
				until_date : 79,
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
			participants_count : 98,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 53,
			color : $client->peerColor(
				color : 39,
				background_emoji_id : -5711604791293550978,
			),
			profile_color : $client->peerColor(
				color : 29,
				background_emoji_id : 244986244345065889,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 75,
			subscription_until_date : 96,
			bot_verification_icon : -4479897330120551721,
			send_paid_messages_stars : -3198292917108105756,
			linked_monoforum_id : -7052261636786059053,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 9066185245530611562,
			access_hash : 8086169364878225071,
			title : 'HsA5MFvpU0PB6j2h',
			until_date : 64,
		),
	),
	users : array(
		$client->userEmpty(
			id : -5728510976024563090,
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
			id : -5508094405235859780,
			access_hash : -2271218293447038314,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 10,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'mYKRBOAq3txeJNz7',
					reason : 'UBc03pAktv62FEmG',
					text : 'tB0MlGR2UIvrjFXD',
				),
			),
			bot_inline_placeholder : 'Z7EvhJYPSmAbctU8',
			lang_code : 'qti6fNsXjAdzw4F2',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 62,
			color : $client->peerColor(
				color : 79,
				background_emoji_id : -6842912682149403014,
			),
			profile_color : $client->peerColor(
				color : 55,
				background_emoji_id : -8499530472720869856,
			),
			bot_active_users : 63,
			bot_verification_icon : 1587856072612355274,
			send_paid_messages_stars : -711905791594625021,
		),
	),
	next_offset : 'k5ZIviXM8s49d6AK',
);
```