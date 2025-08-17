# messages.votesList

**Description** : *How users voted in a poll*

**Layer** : 211

```tl
messages.votesList#4899484e flags:# count:int votes:Vector<MessagePeerVote> chats:Vector<Chat> users:Vector<User> next_offset:flags.0?string = messages.VotesList;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>count</mark> | [`int`](type/int) | Total number of votes for all options (or only for the chosen option, if provided to messages.getPollVotes) |
| <mark>votes</mark> | [`Vector<MessagePeerVote>`](type/MessagePeerVote) | Vote info for each user |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Mentioned chats |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about users that voted in the poll |
| **next_offset** | [`flags.0?string`](type/string) | Offset to use with the next messages.getPollVotes request, empty string if no more results are available |

---

## Type

[messages.VotesList](type/messages.VotesList)

---

## Example

```php
$messagesVotesList = $client->messages->votesList(
	count : 27,
	votes : array(
		$client->messagePeerVote(
			peer : $client->peerUser(
				user_id : 263422386901789024,
			),
			option : 'D?x?HLiveProtoe?ƿX',
			date : 32,
		),
		$client->messagePeerVoteInputOption(
			peer : $client->peerUser(
				user_id : 848727566024281890,
			),
			date : 50,
		),
		$client->messagePeerVoteMultiple(
			peer : $client->peerUser(
				user_id : -8935723706699651971,
			),
			options : array('ol?G?LiveProto??¶'),
			date : 7,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : 6776133502845926430,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : 7564974248862959369,
			title : 'onl6CuXTqwtkz4yD',
			photo : $client->chatPhotoEmpty(),
			participants_count : 89,
			date : 26,
			version : 86,
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
				until_date : 63,
			),
		),
		$client->chatForbidden(
			id : 1252042490645948543,
			title : 'FqhfkniwIKBazUlX',
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
			id : -742262116110491179,
			access_hash : -8851873991912885187,
			title : 'gDQV6ylfkaR91twS',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 18,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'Ja7qwfp50OhrmFXS',
					reason : 'NPo0iHfnZWaA3lFk',
					text : 'tyk46XjlE9RZWVJ1',
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
				until_date : 12,
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
				until_date : 57,
			),
			participants_count : 3,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 55,
			color : $client->peerColor(
				color : 67,
				background_emoji_id : -1951484570928558023,
			),
			profile_color : $client->peerColor(
				color : 21,
				background_emoji_id : 1949357235124721645,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 32,
			subscription_until_date : 79,
			bot_verification_icon : 7799338007272698377,
			send_paid_messages_stars : 7958404248366515277,
			linked_monoforum_id : -4811535894222528778,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : 7287401993914991572,
			access_hash : -6548502251746665668,
			title : 'IDChvs71ygu3UVXQ',
			until_date : 50,
		),
	),
	users : array(
		$client->userEmpty(
			id : -821755930995074597,
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
			id : 5084065399581065750,
			access_hash : -1069328950226103807,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 58,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'EpPMqdG7cyvkKz4t',
					reason : 'V0IiG2lARY6CUf9r',
					text : 'ov7YPIAUQcsdVbkg',
				),
			),
			bot_inline_placeholder : 'zRKJ2NVySxfivq6l',
			lang_code : 'zjXDeMgkCinBvZ5V',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 65,
			color : $client->peerColor(
				color : 44,
				background_emoji_id : -145605382618288672,
			),
			profile_color : $client->peerColor(
				color : 49,
				background_emoji_id : 6992794174721226164,
			),
			bot_active_users : 94,
			bot_verification_icon : -5037924564653741508,
			send_paid_messages_stars : 8320465031543003324,
		),
	),
	next_offset : 'GhdQzCTvn1oRD5cS',
);
```