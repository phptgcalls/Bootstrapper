# chatFull

**Description** : *Full info about a basic group*

**Layer** : 211

```tl
chatFull#2633421b flags:# can_set_username:flags.7?true has_scheduled:flags.8?true translations_disabled:flags.19?true id:long about:string participants:ChatParticipants chat_photo:flags.2?Photo notify_settings:PeerNotifySettings exported_invite:flags.13?ExportedChatInvite bot_info:flags.3?Vector<BotInfo> pinned_msg_id:flags.6?int folder_id:flags.11?int call:flags.12?InputGroupCall ttl_period:flags.14?int groupcall_default_join_as:flags.15?Peer theme_emoticon:flags.16?string requests_pending:flags.17?int recent_requesters:flags.17?Vector<long> available_reactions:flags.18?ChatReactions reactions_limit:flags.20?int = ChatFull;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **can_set_username** | [`flags.7?true`](type/true) | Can we change the username of this chat |
| **has_scheduled** | [`flags.8?true`](type/true) | Whether scheduled messages are available |
| **translations_disabled** | [`flags.19?true`](type/true) | Whether the real-time chat translation popup should be hidden |
| <mark>id</mark> | [`long`](type/long) | ID of the chat |
| <mark>about</mark> | [`string`](type/string) | About string for this chat |
| <mark>participants</mark> | [`ChatParticipants`](type/ChatParticipants) | Participant list |
| **chat_photo** | [`flags.2?Photo`](type/Photo) | Chat photo |
| <mark>notify_settings</mark> | [`PeerNotifySettings`](type/PeerNotifySettings) | Notification settings |
| **exported_invite** | [`flags.13?ExportedChatInvite`](type/ExportedChatInvite) | Chat invite |
| **bot_info** | [`flags.3?Vector<BotInfo>`](type/BotInfo) | Info about bots that are in this chat |
| **pinned_msg_id** | [`flags.6?int`](type/int) | Message ID of the last pinned message |
| **folder_id** | [`flags.11?int`](type/int) | Peer folder ID, for more info click here |
| **call** | [`flags.12?InputGroupCall`](type/InputGroupCall) | Group call information |
| **ttl_period** | [`flags.14?int`](type/int) | Time-To-Live of messages sent by the current user to this chat |
| **groupcall_default_join_as** | [`flags.15?Peer`](type/Peer) | When using phone.getGroupCallJoinAs to get a list of peers that can be used to join a group call, this field indicates the peer that should be selected by default |
| **theme_emoticon** | [`flags.16?string`](type/string) | Emoji representing a specific chat theme |
| **requests_pending** | [`flags.17?int`](type/int) | Pending join requests » |
| **recent_requesters** | [`flags.17?Vector<long>`](type/long) | IDs of users who requested to join recently |
| **available_reactions** | [`flags.18?ChatReactions`](type/ChatReactions) | Allowed message reactions » |
| **reactions_limit** | [`flags.20?int`](type/int) | This flag may be used to impose a custom limit of unique reactions (i.e. a customizable version of appConfig.reactions_uniq_max) |

---

## Type

[ChatFull](type/ChatFull)

---

## Example

```php
$chatFull = $client->chatFull(
	can_set_username : true,
	has_scheduled : true,
	translations_disabled : true,
	id : 3208911624419136440,
	about : 'WzGmZ53F9UKaMyPD',
	participants : $client->chatParticipantsForbidden(
		chat_id : 4869954079905430697,
		self_participant : $client->chatParticipant(
			user_id : -8194396214205870298,
			inviter_id : -7389344194803289319,
			date : 56,
		),
	),
	chat_photo : $client->photoEmpty(
		id : -3818897065342293674,
	),
	notify_settings : $client->peerNotifySettings(
		show_previews : $client->boolFalse(),
		silent : $client->boolFalse(),
		mute_until : 93,
		ios_sound : $client->notificationSoundDefault(),
		android_sound : $client->notificationSoundDefault(),
		other_sound : $client->notificationSoundDefault(),
		stories_muted : $client->boolFalse(),
		stories_hide_sender : $client->boolFalse(),
		stories_ios_sound : $client->notificationSoundDefault(),
		stories_android_sound : $client->notificationSoundDefault(),
		stories_other_sound : $client->notificationSoundDefault(),
	),
	exported_invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'Io864UtRMebNKwla',
		admin_id : -7529763457130336422,
		date : 6,
		start_date : 99,
		expire_date : 28,
		usage_limit : 92,
		usage : 14,
		requested : 27,
		subscription_expired : 45,
		title : 'IUXOfWp6hwszorg7',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 67,
			amount : -5473602866360737307,
		),
	),
	bot_info : array(
		$client->botInfo(
			has_preview_medias : true,
			user_id : -4090596246669446860,
			description : 'WQRPNVIGdksKgbwC',
			description_photo : $client->photoEmpty(
				id : 7928875209086999027,
			),
			description_document : $client->documentEmpty(
				id : 454570704681309123,
			),
			commands : array(
				$client->botCommand(
					command : 'ENf7hSndFXruxm5q',
					description : 'Ixc35rKtzg2QHP4V',
				),
			),
			menu_button : $client->botMenuButtonDefault(),
			privacy_policy_url : 'https://docs.liveproto.dev',
			app_settings : $client->botAppSettings(
				placeholder_path : '
x_M{LiveProto?7N??',
				background_color : 81,
				background_dark_color : 52,
				header_color : 86,
				header_dark_color : 82,
			),
			verifier_settings : $client->botVerifierSettings(
				can_modify_custom_description : true,
				icon : 6500657140778938933,
				company : 'Che23aZbgWmfYE6G',
				custom_description : 'qAg0tzP1wCSnhuvL',
			),
		),
	),
	pinned_msg_id : 63,
	folder_id : 39,
	call : $client->inputGroupCall(
		id : -2546884963693186851,
		access_hash : 713737683586369896,
	),
	ttl_period : 44,
	groupcall_default_join_as : $client->peerUser(
		user_id : 1407075435929202576,
	),
	theme_emoticon : 'zZGQ0ndB2FRhlgXL',
	requests_pending : 44,
	recent_requesters : array(-3895954372144415582),
	available_reactions : $client->chatReactionsNone(),
	reactions_limit : 32,
);
```