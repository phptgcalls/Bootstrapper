# peerStories

**Description** : *Stories associated to a peer*

**Layer** : 211

```tl
peerStories#9a35e999 flags:# peer:Peer max_read_id:flags.0?int stories:Vector<StoryItem> = PeerStories;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>peer</mark> | [`Peer`](type/Peer) | The peer |
| **max_read_id** | [`flags.0?int`](type/int) | If set, contains the ID of the maximum read story |
| <mark>stories</mark> | [`Vector<StoryItem>`](type/StoryItem) | Stories |

---

## Type

[PeerStories](type/PeerStories)

---

## Example

```php
$peerStories = $client->peerStories(
	peer : $client->peerUser(
		user_id : -1515110712542789566,
	),
	max_read_id : 20,
	stories : array(
		$client->storyItemDeleted(
			id : 88,
		),
		$client->storyItemSkipped(
			close_friends : true,
			id : 87,
			date : 34,
			expire_date : 88,
		),
		$client->storyItem(
			pinned : true,
			public : true,
			close_friends : true,
			min : true,
			noforwards : true,
			edited : true,
			contacts : true,
			selected_contacts : true,
			out : true,
			id : 65,
			date : 65,
			from_id : $client->peerUser(
				user_id : 7864430848873181888,
			),
			fwd_from : $client->storyFwdHeader(
				modified : true,
				from : $client->peerUser(...),
				from_name : 'Afnk02HqIDlbhNSW',
				story_id : 30,
			),
			expire_date : 5,
			caption : 'A21fEDvh4RxeX3tF',
			entities : array(
				$client->messageEntityUnknown(
					offset : 41,
					length : 45,
				),
				$client->messageEntityMention(
					offset : 9,
					length : 8,
				),
				$client->messageEntityHashtag(
					offset : 14,
					length : 73,
				),
				$client->messageEntityBotCommand(
					offset : 88,
					length : 64,
				),
				$client->messageEntityUrl(
					offset : 59,
					length : 37,
				),
				$client->messageEntityEmail(
					offset : 58,
					length : 32,
				),
				$client->messageEntityBold(
					offset : 81,
					length : 52,
				),
				$client->messageEntityItalic(
					offset : 89,
					length : 41,
				),
				$client->messageEntityCode(
					offset : 21,
					length : 95,
				),
				$client->messageEntityPre(
					offset : 63,
					length : 27,
					language : 'zKw7LHh5pgP1feIs',
				),
				$client->messageEntityTextUrl(
					offset : 91,
					length : 45,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 43,
					length : 65,
					user_id : -8074209816752353315,
				),
				$client->inputMessageEntityMentionName(
					offset : 43,
					length : 5,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 51,
					length : 79,
				),
				$client->messageEntityCashtag(
					offset : 35,
					length : 90,
				),
				$client->messageEntityUnderline(
					offset : 52,
					length : 76,
				),
				$client->messageEntityStrike(
					offset : 42,
					length : 61,
				),
				$client->messageEntityBankCard(
					offset : 13,
					length : 30,
				),
				$client->messageEntitySpoiler(
					offset : 14,
					length : 73,
				),
				$client->messageEntityCustomEmoji(
					offset : 4,
					length : 44,
					document_id : 5742738858163405074,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 67,
					length : 55,
				),
			),
			media : $client->messageMediaEmpty(),
			media_areas : array(
				$client->mediaAreaVenue(
					coordinates : $client->mediaAreaCoordinates(...),
					geo : $client->geoPointEmpty(...),
					title : 'XEn69sbB0g7eYd5i',
					address : 'xWiTkCMz4eb1DUVK',
					provider : 'E814iJ6NxMF2PYL9',
					venue_id : 'w6XuyY7TWz1nHvjF',
					venue_type : 'feKIUjviSDzFNs4o',
				),
				$client->inputMediaAreaVenue(
					coordinates : $client->mediaAreaCoordinates(...),
					query_id : 4979477148491312852,
					result_id : 'LzK734aJ6kp2PVNW',
				),
				$client->mediaAreaGeoPoint(
					coordinates : $client->mediaAreaCoordinates(...),
					geo : $client->geoPointEmpty(...),
					address : $client->geoPointAddress(...),
				),
				$client->mediaAreaSuggestedReaction(
					dark : true,
					flipped : true,
					coordinates : $client->mediaAreaCoordinates(...),
					reaction : $client->reactionEmpty(...),
				),
				$client->mediaAreaChannelPost(
					coordinates : $client->mediaAreaCoordinates(...),
					channel_id : 7671267261138483058,
					msg_id : 75,
				),
				$client->inputMediaAreaChannelPost(
					coordinates : $client->mediaAreaCoordinates(...),
					channel : $client->inputChannelEmpty(...),
					msg_id : 0,
				),
				$client->mediaAreaUrl(
					coordinates : $client->mediaAreaCoordinates(...),
					url : 'https://docs.liveproto.dev',
				),
				$client->mediaAreaWeather(
					coordinates : $client->mediaAreaCoordinates(...),
					emoji : 'tgMqFfDKPaJ3nTzy',
					temperature_c : 849574.123046875,
					color : 59,
				),
				$client->mediaAreaStarGift(
					coordinates : $client->mediaAreaCoordinates(...),
					slug : 'RZHaQ914FlEkBzuh',
				),
			),
			privacy : array(
				$client->privacyValueAllowContacts(),
				$client->privacyValueAllowAll(),
				$client->privacyValueAllowUsers(
					users : array(3140401437134578872),
				),
				$client->privacyValueDisallowContacts(),
				$client->privacyValueDisallowAll(),
				$client->privacyValueDisallowUsers(
					users : array(4717019367922227071),
				),
				$client->privacyValueAllowChatParticipants(
					chats : array(9200920933116303417),
				),
				$client->privacyValueDisallowChatParticipants(
					chats : array(-1588038654313119689),
				),
				$client->privacyValueAllowCloseFriends(),
				$client->privacyValueAllowPremium(),
				$client->privacyValueAllowBots(),
				$client->privacyValueDisallowBots(),
			),
			views : $client->storyViews(
				has_viewers : true,
				views_count : 98,
				forwards_count : 0,
				reactions : array(
					$client->reactionCount(...),
				),
				reactions_count : 47,
				recent_viewers : array(3229359155162285409),
			),
			sent_reaction : $client->reactionEmpty(),
			albums : array(77),
		),
	),
);
```