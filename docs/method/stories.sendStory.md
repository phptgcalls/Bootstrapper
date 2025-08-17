# stories.sendStory

**Description** : *Uploads a Telegram Story*

**Layer** : 211

```tl
stories.sendStory#737fc2ec flags:# pinned:flags.2?true noforwards:flags.4?true fwd_modified:flags.7?true peer:InputPeer media:InputMedia media_areas:flags.5?Vector<MediaArea> caption:flags.0?string entities:flags.1?Vector<MessageEntity> privacy_rules:Vector<InputPrivacyRule> random_id:long period:flags.3?int fwd_from_id:flags.6?InputPeer fwd_from_story:flags.6?int albums:flags.8?Vector<int> = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **pinned** | [`flags.2?true`](type/true) | Whether to add the story to the profile automatically upon expiration. If not set, the story will only be added to the archive, see here » for more info |
| **noforwards** | [`flags.4?true`](type/true) | If set, disables forwards, screenshots, and downloads |
| **fwd_modified** | [`flags.7?true`](type/true) | Set this flag when reposting stories with fwd_from_id+fwd_from_id, if the media was modified before reposting |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | The peer to send the story as |
| <mark>media</mark> | [`InputMedia`](type/InputMedia) | The story media |
| **media_areas** | [`flags.5?Vector<MediaArea>`](type/MediaArea) | Media areas associated to the story, see here » for more info |
| **caption** | [`flags.0?string`](type/string) | Story caption |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text, if allowed by the stories_entities client configuration parameter » |
| <mark>privacy_rules</mark> | [`Vector<InputPrivacyRule>`](type/InputPrivacyRule) | Privacy rules for the story, indicating who can or can't view the story |
| <mark>random_id</mark> | [`long`](type/long) | Unique client message ID required to prevent message resending |
| **period** | [`flags.3?int`](type/int) | Period after which the story is moved to archive (and to the profile if pinned is set), in seconds; must be one of 6 * 3600, 12 * 3600, 86400, or 2 * 86400 for Telegram Premium users, and 86400 otherwise |
| **fwd_from_id** | [`flags.6?InputPeer`](type/InputPeer) | If set, indicates that this story is a repost of story with ID fwd_from_story posted by the peer in fwd_from_id |
| **fwd_from_story** | [`flags.6?int`](type/int) | If set, indicates that this story is a repost of story with ID fwd_from_story posted by the peer in fwd_from_id |
| **albums** | [`flags.8?Vector<int>`](type/int) | NOTHING |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **BOOSTS_REQUIRED** | `400` | The specified channel must first be boosted by its users in order to perform this action |
| **IMAGE_PROCESS_FAILED** | `400` | Failure while processing image |
| **MEDIA_EMPTY** | `400` | The provided media object is invalid |
| **MEDIA_FILE_INVALID** | `400` | The specified media file is invalid |
| **MEDIA_TYPE_INVALID** | `400` | The specified media type cannot be used in stories |
| **MEDIA_VIDEO_STORY_MISSING** | `400` | A non-story video cannot be repubblished as a story (emitted when trying to resend a non-story video as a story using inputDocument) |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |
| **PREMIUM_ACCOUNT_REQUIRED** | `400` | A premium account is required to execute this action |
| **STORIES_TOO_MUCH** | `400` | You have hit the maximum active stories limit as specified by the story_expiring_limit_* client configuration parameters: you should buy a Premium subscription, delete an active story, or wait for the oldest story to expire |
| **STORY_PERIOD_INVALID** | `400` | The specified story period is invalid for this account |
| **VENUE_ID_INVALID** | `400` | The specified venue ID is invalid |

---

## Example

```php
$updates = $client->stories->sendStory(
	pinned : true,
	noforwards : true,
	fwd_modified : true,
	peer : $client->inputPeerEmpty(),
	media : $client->inputMediaEmpty(),
	media_areas : array(
		$client->mediaAreaVenue(
			coordinates : $client->mediaAreaCoordinates(
				x : -1575464.9755859375,
				y : 254006.76953125,
				w : -528696.7294921875,
				h : -476024.892578125,
				rotation : -1614872.822265625,
				radius : -94087.9580078125,
			),
			geo : $client->geoPointEmpty(),
			title : 'F4SuHqOR2NWdXcxz',
			address : 'ZJzhjFnTUAPyYROk',
			provider : 'yoqKiTMZeh5FWaHn',
			venue_id : 'gzEhJ521jGLCxFbf',
			venue_type : '8L3Ofonb4ilrRJek',
		),
		$client->inputMediaAreaVenue(
			coordinates : $client->mediaAreaCoordinates(
				x : -1618202.5830078125,
				y : 2034999.048828125,
				w : 863118.755859375,
				h : -718901.228515625,
				rotation : 1061624.037109375,
				radius : -596519.7880859375,
			),
			query_id : -940295859868535640,
			result_id : 's9rflRC4USW3XtiT',
		),
		$client->mediaAreaGeoPoint(
			coordinates : $client->mediaAreaCoordinates(
				x : -1739116.6259765625,
				y : -1465301.3359375,
				w : -1519585.18359375,
				h : -2035439.7470703125,
				rotation : 631343.404296875,
				radius : -1925373.404296875,
			),
			geo : $client->geoPointEmpty(),
			address : $client->geoPointAddress(
				country_iso2 : 'lOegZBUXdxJAncQb',
				state : 'RBFy40OPuxeXQsKc',
				city : 'GRBxbV06JnTocUIq',
				street : '2URaV8vXdp3ukIDh',
			),
		),
		$client->mediaAreaSuggestedReaction(
			dark : true,
			flipped : true,
			coordinates : $client->mediaAreaCoordinates(
				x : 1769293.533203125,
				y : 861906.369140625,
				w : -1268394.66015625,
				h : -155097.2783203125,
				rotation : -47818.076171875,
				radius : 1512192.224609375,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->mediaAreaChannelPost(
			coordinates : $client->mediaAreaCoordinates(
				x : -986399.4326171875,
				y : 40058.9306640625,
				w : -125769.7109375,
				h : -1885007.4306640625,
				rotation : -1963286.97265625,
				radius : -1530350.7880859375,
			),
			channel_id : 4902860433680314834,
			msg_id : 13,
		),
		$client->inputMediaAreaChannelPost(
			coordinates : $client->mediaAreaCoordinates(
				x : -65557.5,
				y : -1800830.396484375,
				w : -1784507.5068359375,
				h : -159729.4033203125,
				rotation : -1138859.5693359375,
				radius : 256906.50390625,
			),
			channel : $client->inputChannelEmpty(),
			msg_id : 85,
		),
		$client->mediaAreaUrl(
			coordinates : $client->mediaAreaCoordinates(
				x : 391765.109375,
				y : -1218956.1015625,
				w : -1395947.9716796875,
				h : 772751.8388671875,
				rotation : 1386655.693359375,
				radius : -195882.423828125,
			),
			url : 'https://docs.liveproto.dev',
		),
		$client->mediaAreaWeather(
			coordinates : $client->mediaAreaCoordinates(
				x : 1594965.138671875,
				y : 661747.228515625,
				w : 70201.3564453125,
				h : 383998.359375,
				rotation : -334457.4951171875,
				radius : -409954.546875,
			),
			emoji : 'BT5nizNCguYAq2yd',
			temperature_c : 1839709.8955078125,
			color : 21,
		),
		$client->mediaAreaStarGift(
			coordinates : $client->mediaAreaCoordinates(
				x : -1722406.5849609375,
				y : 1747978.9130859375,
				w : -832559.6064453125,
				h : -1982609.251953125,
				rotation : -1051235.001953125,
				radius : -1536331.041015625,
			),
			slug : '7gJNtkcECmh3aBvj',
		),
	),
	caption : 'ck79mgyMntRJ5Dso',
	entities : array(
		$client->messageEntityUnknown(
			offset : 33,
			length : 71,
		),
		$client->messageEntityMention(
			offset : 76,
			length : 0,
		),
		$client->messageEntityHashtag(
			offset : 68,
			length : 39,
		),
		$client->messageEntityBotCommand(
			offset : 35,
			length : 37,
		),
		$client->messageEntityUrl(
			offset : 43,
			length : 60,
		),
		$client->messageEntityEmail(
			offset : 72,
			length : 100,
		),
		$client->messageEntityBold(
			offset : 2,
			length : 80,
		),
		$client->messageEntityItalic(
			offset : 58,
			length : 13,
		),
		$client->messageEntityCode(
			offset : 2,
			length : 7,
		),
		$client->messageEntityPre(
			offset : 62,
			length : 97,
			language : 'DTgvFcMs91yY7Nnj',
		),
		$client->messageEntityTextUrl(
			offset : 47,
			length : 65,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 90,
			length : 95,
			user_id : 6886711937313303533,
		),
		$client->inputMessageEntityMentionName(
			offset : 10,
			length : 51,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 70,
			length : 7,
		),
		$client->messageEntityCashtag(
			offset : 25,
			length : 39,
		),
		$client->messageEntityUnderline(
			offset : 63,
			length : 83,
		),
		$client->messageEntityStrike(
			offset : 28,
			length : 35,
		),
		$client->messageEntityBankCard(
			offset : 46,
			length : 27,
		),
		$client->messageEntitySpoiler(
			offset : 93,
			length : 71,
		),
		$client->messageEntityCustomEmoji(
			offset : 8,
			length : 45,
			document_id : 2101230852939978826,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 14,
			length : 53,
		),
	),
	privacy_rules : array(
		$client->inputPrivacyValueAllowContacts(),
		$client->inputPrivacyValueAllowAll(),
		$client->inputPrivacyValueAllowUsers(
			users : array(
				$client->inputUserEmpty(),
				$client->inputUserSelf(),
				$client->inputUser(
					user_id : 8109296103311430332,
					access_hash : -1381634807410395338,
				),
				$client->inputUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 5,
					user_id : -5849403670876465411,
				),
			),
		),
		$client->inputPrivacyValueDisallowContacts(),
		$client->inputPrivacyValueDisallowAll(),
		$client->inputPrivacyValueDisallowUsers(
			users : array(
				$client->inputUserEmpty(),
				$client->inputUserSelf(),
				$client->inputUser(
					user_id : -369871096577157284,
					access_hash : 3857458003358570054,
				),
				$client->inputUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 80,
					user_id : -7024547509063542932,
				),
			),
		),
		$client->inputPrivacyValueAllowChatParticipants(
			chats : array(4273213351909819567),
		),
		$client->inputPrivacyValueDisallowChatParticipants(
			chats : array(-8487869287848614416),
		),
		$client->inputPrivacyValueAllowCloseFriends(),
		$client->inputPrivacyValueAllowPremium(),
		$client->inputPrivacyValueAllowBots(),
		$client->inputPrivacyValueDisallowBots(),
	),
	random_id : -5547835640837550528,
	period : 15,
	fwd_from_id : $client->inputPeerEmpty(),
	fwd_from_story : 94,
	albums : array(23),
);
```