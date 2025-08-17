# storyItem

**Description** : *Represents a story*

**Layer** : 211

```tl
storyItem#edf164f1 flags:# pinned:flags.5?true public:flags.7?true close_friends:flags.8?true min:flags.9?true noforwards:flags.10?true edited:flags.11?true contacts:flags.12?true selected_contacts:flags.13?true out:flags.16?true id:int date:int from_id:flags.18?Peer fwd_from:flags.17?StoryFwdHeader expire_date:int caption:flags.0?string entities:flags.1?Vector<MessageEntity> media:MessageMedia media_areas:flags.14?Vector<MediaArea> privacy:flags.2?Vector<PrivacyRule> views:flags.3?StoryViews sent_reaction:flags.15?Reaction albums:flags.19?Vector<int> = StoryItem;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **pinned** | [`flags.5?true`](type/true) | Whether this story is pinned on the user's profile |
| **public** | [`flags.7?true`](type/true) | Whether this story is public and can be viewed by everyone |
| **close_friends** | [`flags.8?true`](type/true) | Whether this story can only be viewed by our close friends, see here » for more info |
| **min** | [`flags.9?true`](type/true) | Full information about this story was omitted for space and performance reasons; use stories.getStoriesByID to fetch full info about this story when and if needed |
| **noforwards** | [`flags.10?true`](type/true) | Whether this story is protected and thus cannot be forwarded; clients should also prevent users from saving attached media (i.e. videos should only be streamed, photos should be kept in RAM, et cetera) |
| **edited** | [`flags.11?true`](type/true) | Indicates whether the story was edited |
| **contacts** | [`flags.12?true`](type/true) | Whether this story can only be viewed by our contacts |
| **selected_contacts** | [`flags.13?true`](type/true) | Whether this story can only be viewed by a select list of our contacts |
| **out** | [`flags.16?true`](type/true) | indicates whether we sent this story |
| <mark>id</mark> | [`int`](type/int) | ID of the story |
| <mark>date</mark> | [`int`](type/int) | When was the story posted |
| **from_id** | [`flags.18?Peer`](type/Peer) | Sender of the story |
| **fwd_from** | [`flags.17?StoryFwdHeader`](type/StoryFwdHeader) | For reposted stories », contains info about the original story |
| <mark>expire_date</mark> | [`int`](type/int) | When does the story expire |
| **caption** | [`flags.0?string`](type/string) | Story caption |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |
| <mark>media</mark> | [`MessageMedia`](type/MessageMedia) | Story media |
| **media_areas** | [`flags.14?Vector<MediaArea>`](type/MediaArea) | List of media areas, see here » for more info on media areas |
| **privacy** | [`flags.2?Vector<PrivacyRule>`](type/PrivacyRule) | Privacy rules indicating who can and can't view this story |
| **views** | [`flags.3?StoryViews`](type/StoryViews) | View date and reaction information |
| **sent_reaction** | [`flags.15?Reaction`](type/Reaction) | The reaction we sent |
| **albums** | [`flags.19?Vector<int>`](type/int) | NOTHING |

---

## Type

[StoryItem](type/StoryItem)

---

## Example

```php
$storyItem = $client->storyItem(
	pinned : true,
	public : true,
	close_friends : true,
	min : true,
	noforwards : true,
	edited : true,
	contacts : true,
	selected_contacts : true,
	out : true,
	id : 62,
	date : 41,
	from_id : $client->peerUser(
		user_id : -113925467554281706,
	),
	fwd_from : $client->storyFwdHeader(
		modified : true,
		from : $client->peerUser(
			user_id : -1734544503751808866,
		),
		from_name : 'yI6xg8kTXzq3VNK1',
		story_id : 1,
	),
	expire_date : 40,
	caption : '2SEk4ydpevhjXG1L',
	entities : array(
		$client->messageEntityUnknown(
			offset : 46,
			length : 94,
		),
		$client->messageEntityMention(
			offset : 19,
			length : 59,
		),
		$client->messageEntityHashtag(
			offset : 83,
			length : 43,
		),
		$client->messageEntityBotCommand(
			offset : 9,
			length : 58,
		),
		$client->messageEntityUrl(
			offset : 96,
			length : 88,
		),
		$client->messageEntityEmail(
			offset : 71,
			length : 50,
		),
		$client->messageEntityBold(
			offset : 27,
			length : 42,
		),
		$client->messageEntityItalic(
			offset : 3,
			length : 66,
		),
		$client->messageEntityCode(
			offset : 5,
			length : 89,
		),
		$client->messageEntityPre(
			offset : 70,
			length : 99,
			language : 'MD9LzU1h6tklxBZp',
		),
		$client->messageEntityTextUrl(
			offset : 44,
			length : 38,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 86,
			length : 14,
			user_id : 8177785091471451321,
		),
		$client->inputMessageEntityMentionName(
			offset : 70,
			length : 89,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 23,
			length : 23,
		),
		$client->messageEntityCashtag(
			offset : 5,
			length : 29,
		),
		$client->messageEntityUnderline(
			offset : 37,
			length : 58,
		),
		$client->messageEntityStrike(
			offset : 71,
			length : 17,
		),
		$client->messageEntityBankCard(
			offset : 79,
			length : 66,
		),
		$client->messageEntitySpoiler(
			offset : 74,
			length : 41,
		),
		$client->messageEntityCustomEmoji(
			offset : 90,
			length : 35,
			document_id : 3955943913976362499,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 93,
			length : 97,
		),
	),
	media : $client->messageMediaEmpty(),
	media_areas : array(
		$client->mediaAreaVenue(
			coordinates : $client->mediaAreaCoordinates(
				x : 16497.5966796875,
				y : -1702310.7314453125,
				w : -871300.7197265625,
				h : 1690850.201171875,
				rotation : 1390169.345703125,
				radius : 1123837.5419921875,
			),
			geo : $client->geoPointEmpty(),
			title : 'c04736BfOhpXxNsS',
			address : 'PQ1tNWUMXB8w7yEv',
			provider : 'TH02kYXMNtrDuoF6',
			venue_id : 'Ycby6EjloepwhSJN',
			venue_type : 'aweHnEd5RQZGbTMF',
		),
		$client->inputMediaAreaVenue(
			coordinates : $client->mediaAreaCoordinates(
				x : -2049284.2626953125,
				y : 1425586.2021484375,
				w : -1266869.1279296875,
				h : 1871321.8681640625,
				rotation : 1986168.0869140625,
				radius : 1037255.888671875,
			),
			query_id : 2673010555465025346,
			result_id : 'Rn6xuT3ig4rhdIOy',
		),
		$client->mediaAreaGeoPoint(
			coordinates : $client->mediaAreaCoordinates(
				x : 1891677.7236328125,
				y : 996333.1318359375,
				w : 8555.091796875,
				h : 1905150.90625,
				rotation : 1984793.427734375,
				radius : -1593155.0771484375,
			),
			geo : $client->geoPointEmpty(),
			address : $client->geoPointAddress(
				country_iso2 : 'SvuOs7KHtwVQnplB',
				state : 'wAYleGudLspF3zmJ',
				city : 'WcxiUAFEq9BfrKVb',
				street : 'YGPKvBxu9z4ReImk',
			),
		),
		$client->mediaAreaSuggestedReaction(
			dark : true,
			flipped : true,
			coordinates : $client->mediaAreaCoordinates(
				x : -1047388.4384765625,
				y : 1935263.5185546875,
				w : -938062.01171875,
				h : -183029.896484375,
				rotation : 33106.1162109375,
				radius : 21023.7421875,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->mediaAreaChannelPost(
			coordinates : $client->mediaAreaCoordinates(
				x : 518429.013671875,
				y : -222054.3525390625,
				w : -1381098.873046875,
				h : -1398640.37890625,
				rotation : -1776645.3291015625,
				radius : 517232.755859375,
			),
			channel_id : 6733455188664229056,
			msg_id : 90,
		),
		$client->inputMediaAreaChannelPost(
			coordinates : $client->mediaAreaCoordinates(
				x : 416380.0390625,
				y : -913460.783203125,
				w : 2096428.5654296875,
				h : -1799478.8671875,
				rotation : 252838.6953125,
				radius : -1942272.4267578125,
			),
			channel : $client->inputChannelEmpty(),
			msg_id : 95,
		),
		$client->mediaAreaUrl(
			coordinates : $client->mediaAreaCoordinates(
				x : -716630.310546875,
				y : 1615124.802734375,
				w : 754385.1484375,
				h : 830365.5859375,
				rotation : -636813.2548828125,
				radius : 546616.7822265625,
			),
			url : 'https://docs.liveproto.dev',
		),
		$client->mediaAreaWeather(
			coordinates : $client->mediaAreaCoordinates(
				x : 262100.0615234375,
				y : 1856437.546875,
				w : 1719419.1025390625,
				h : 22494.369140625,
				rotation : -1603363.1640625,
				radius : 1305017.810546875,
			),
			emoji : 'odtRF8ZJ6vCNEhyw',
			temperature_c : 926547.1416015625,
			color : 19,
		),
		$client->mediaAreaStarGift(
			coordinates : $client->mediaAreaCoordinates(
				x : -1602710.634765625,
				y : 1203566.0732421875,
				w : 686603.5771484375,
				h : 1063533.7451171875,
				rotation : -1639346.1298828125,
				radius : -1986201.513671875,
			),
			slug : '7sbMGDgnmKRjaY8V',
		),
	),
	privacy : array(
		$client->privacyValueAllowContacts(),
		$client->privacyValueAllowAll(),
		$client->privacyValueAllowUsers(
			users : array(7814404501533428545),
		),
		$client->privacyValueDisallowContacts(),
		$client->privacyValueDisallowAll(),
		$client->privacyValueDisallowUsers(
			users : array(-8445656292907286767),
		),
		$client->privacyValueAllowChatParticipants(
			chats : array(-7380453925517093439),
		),
		$client->privacyValueDisallowChatParticipants(
			chats : array(-2256742939406687189),
		),
		$client->privacyValueAllowCloseFriends(),
		$client->privacyValueAllowPremium(),
		$client->privacyValueAllowBots(),
		$client->privacyValueDisallowBots(),
	),
	views : $client->storyViews(
		has_viewers : true,
		views_count : 73,
		forwards_count : 90,
		reactions : array(
			$client->reactionCount(
				chosen_order : 0,
				reaction : $client->reactionEmpty(...),
				count : 50,
			),
		),
		reactions_count : 0,
		recent_viewers : array(-5046514685860881429),
	),
	sent_reaction : $client->reactionEmpty(),
	albums : array(50),
);
```