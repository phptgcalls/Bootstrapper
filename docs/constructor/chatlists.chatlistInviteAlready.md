# chatlists.chatlistInviteAlready

**Description** : *Updated info about a chat folder deep link » we already imported*

**Layer** : 211

```tl
chatlists.chatlistInviteAlready#fa87f659 filter_id:int missing_peers:Vector<Peer> already_peers:Vector<Peer> chats:Vector<Chat> users:Vector<User> = chatlists.ChatlistInvite;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>filter_id</mark> | [`int`](type/int) | ID of the imported folder |
| <mark>missing_peers</mark> | [`Vector<Peer>`](type/Peer) | New peers to be imported |
| <mark>already_peers</mark> | [`Vector<Peer>`](type/Peer) | Peers that were already imported |
| <mark>chats</mark> | [`Vector<Chat>`](type/Chat) | Related chat information |
| <mark>users</mark> | [`Vector<User>`](type/User) | Related user information |

---

## Type

[chatlists.ChatlistInvite](type/chatlists.ChatlistInvite)

---

## Example

```php
$chatlistsChatlistInvite = $client->chatlists->chatlistInviteAlready(
	filter_id : 28,
	missing_peers : array(
		$client->peerUser(
			user_id : 8506628377501431408,
		),
		$client->peerChat(
			chat_id : -1606570936741438769,
		),
		$client->peerChannel(
			channel_id : -6854417745171839877,
		),
	),
	already_peers : array(
		$client->peerUser(
			user_id : -376773679812659402,
		),
		$client->peerChat(
			chat_id : 3759967660842460500,
		),
		$client->peerChannel(
			channel_id : -6635484456556630255,
		),
	),
	chats : array(
		$client->chatEmpty(
			id : -1193403489109304669,
		),
		$client->chat(
			creator : true,
			left : true,
			deactivated : true,
			call_active : true,
			call_not_empty : true,
			noforwards : true,
			id : -2577689913388483622,
			title : 'UPR2IhVEG1mr3qSL',
			photo : $client->chatPhotoEmpty(),
			participants_count : 60,
			date : 66,
			version : 91,
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
				until_date : 12,
			),
		),
		$client->chatForbidden(
			id : -7657330087409876791,
			title : 'gZitYoGaq8zjEFlk',
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
			id : -5217074772302360029,
			access_hash : 2967358390972005609,
			title : 'hUdpA1VcqgLytFar',
			username : 'TakNone',
			photo : $client->chatPhotoEmpty(),
			date : 8,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'HNYvz6EWDI3UVTO8',
					reason : 'v6r4inuFUV0gENkG',
					text : 'JAnwsBOMYaGpTgHd',
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
				until_date : 82,
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
			participants_count : 71,
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 76,
			color : $client->peerColor(
				color : 100,
				background_emoji_id : 1441753822151833606,
			),
			profile_color : $client->peerColor(
				color : 0,
				background_emoji_id : 438875836361404374,
			),
			emoji_status : $client->emojiStatusEmpty(),
			level : 76,
			subscription_until_date : 84,
			bot_verification_icon : -6569494266090396127,
			send_paid_messages_stars : 3908049406754005314,
			linked_monoforum_id : 3845762717029232499,
		),
		$client->channelForbidden(
			broadcast : true,
			megagroup : true,
			id : -3278815062040868695,
			access_hash : -2452682870607237175,
			title : 'azXfixPIj4K10lSD',
			until_date : 55,
		),
	),
	users : array(
		$client->userEmpty(
			id : -1340659612143662085,
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
			id : 6210771646906374469,
			access_hash : -8962736770952531941,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 26,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'WAoSlYarepgxqIk5',
					reason : '0ELoY2eD9pC451RM',
					text : 'hdLOX3o2Yj6evgQE',
				),
			),
			bot_inline_placeholder : '03lL2OuhSREPeQFG',
			lang_code : '61EACwRJyshDQeKF',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 95,
			color : $client->peerColor(
				color : 54,
				background_emoji_id : -7663089765953295342,
			),
			profile_color : $client->peerColor(
				color : 65,
				background_emoji_id : 1251969042580077644,
			),
			bot_active_users : 73,
			bot_verification_icon : -6660651559213389041,
			send_paid_messages_stars : -2087551487793709777,
		),
	),
);
```