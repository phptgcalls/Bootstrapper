# stories.editStory

**Description** : *Edit an uploaded story*

**Layer** : 211

```tl
stories.editStory#b583ba46 flags:# peer:InputPeer id:int media:flags.0?InputMedia media_areas:flags.3?Vector<MediaArea> caption:flags.1?string entities:flags.1?Vector<MessageEntity> privacy_rules:flags.2?Vector<InputPrivacyRule> = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Peer where the story was posted |
| <mark>id</mark> | [`int`](type/int) | ID of story to edit |
| **media** | [`flags.0?InputMedia`](type/InputMedia) | If specified, replaces the story media |
| **media_areas** | [`flags.3?Vector<MediaArea>`](type/MediaArea) | Media areas associated to the story, see here » for more info |
| **caption** | [`flags.1?string`](type/string) | If specified, replaces the story caption |
| **entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text in the caption, if allowed by the stories_entities client configuration parameter » |
| **privacy_rules** | [`flags.2?Vector<InputPrivacyRule>`](type/InputPrivacyRule) | If specified, alters the privacy settings » of the story, changing who can or can't view the story |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |
| **STORY_NOT_MODIFIED** | `400` | The new story information you passed is equal to the previous story information, thus it wasn't modified |

---

## Example

```php
$updates = $client->stories->editStory(
	peer : $client->inputPeerEmpty(),
	id : 35,
	media : $client->inputMediaEmpty(),
	media_areas : array(
		$client->mediaAreaVenue(
			coordinates : $client->mediaAreaCoordinates(
				x : 804047.580078125,
				y : -1931685.4052734375,
				w : -254602.26953125,
				h : 938520.6064453125,
				rotation : 881399.0166015625,
				radius : 238454.17578125,
			),
			geo : $client->geoPointEmpty(),
			title : 'xXbNVfjdQFRsBAGg',
			address : 'Ly38bFAg0hYoxWmO',
			provider : 'ACgwTKXhbLjnDieY',
			venue_id : 'bGjJyYMt9qHD1Qr7',
			venue_type : 'r524qVcOnBw08NTu',
		),
		$client->inputMediaAreaVenue(
			coordinates : $client->mediaAreaCoordinates(
				x : 581167.9267578125,
				y : 1687250.24609375,
				w : -262534.224609375,
				h : -732728.33203125,
				rotation : 1245690.4228515625,
				radius : 216423.84765625,
			),
			query_id : 6241798502019131285,
			result_id : '0iT1vl2QmysoVA3X',
		),
		$client->mediaAreaGeoPoint(
			coordinates : $client->mediaAreaCoordinates(
				x : 568192.287109375,
				y : -124163.90625,
				w : 658379.3857421875,
				h : 1274002.0791015625,
				rotation : 995825.9033203125,
				radius : -1116186.1376953125,
			),
			geo : $client->geoPointEmpty(),
			address : $client->geoPointAddress(
				country_iso2 : 'mHDSIulNc6yn8Rqh',
				state : 'sWBcrixqNenQXlvF',
				city : '1I5RfxgTzw20HLc6',
				street : 'z5vPJgwCiAtfhYs3',
			),
		),
		$client->mediaAreaSuggestedReaction(
			dark : true,
			flipped : true,
			coordinates : $client->mediaAreaCoordinates(
				x : -785340.83984375,
				y : -1181799.6279296875,
				w : 36835.3525390625,
				h : 1443962.984375,
				rotation : -863861.9365234375,
				radius : 740457.2685546875,
			),
			reaction : $client->reactionEmpty(),
		),
		$client->mediaAreaChannelPost(
			coordinates : $client->mediaAreaCoordinates(
				x : -1850083.185546875,
				y : -735864.130859375,
				w : -1664757.607421875,
				h : 1706565.0341796875,
				rotation : 565613.0478515625,
				radius : -1403499.998046875,
			),
			channel_id : 7976062643598377279,
			msg_id : 93,
		),
		$client->inputMediaAreaChannelPost(
			coordinates : $client->mediaAreaCoordinates(
				x : -695634.0693359375,
				y : -1241130.330078125,
				w : -740257.7763671875,
				h : -282077.111328125,
				rotation : -1618090.890625,
				radius : 1395830.158203125,
			),
			channel : $client->inputChannelEmpty(),
			msg_id : 99,
		),
		$client->mediaAreaUrl(
			coordinates : $client->mediaAreaCoordinates(
				x : 497758.4130859375,
				y : -1725939.181640625,
				w : 470152.1669921875,
				h : 1135045.4697265625,
				rotation : -788507.6396484375,
				radius : 475732.6982421875,
			),
			url : 'https://docs.liveproto.dev',
		),
		$client->mediaAreaWeather(
			coordinates : $client->mediaAreaCoordinates(
				x : 1178954.9423828125,
				y : -684423.4384765625,
				w : -1543706.1572265625,
				h : -1782725.888671875,
				rotation : -881662.94140625,
				radius : -1011893.8388671875,
			),
			emoji : 'Glu5EWwUTBOnjbzm',
			temperature_c : -716444.125,
			color : 0,
		),
		$client->mediaAreaStarGift(
			coordinates : $client->mediaAreaCoordinates(
				x : -1338734.0244140625,
				y : -179986.9482421875,
				w : -1376628.48046875,
				h : -717181.509765625,
				rotation : 52982.642578125,
				radius : 1362446.654296875,
			),
			slug : '04t3RgvKkdoiYfNc',
		),
	),
	caption : 'wvb02KhCfHqx1ouI',
	entities : array(
		$client->messageEntityUnknown(
			offset : 64,
			length : 3,
		),
		$client->messageEntityMention(
			offset : 39,
			length : 8,
		),
		$client->messageEntityHashtag(
			offset : 13,
			length : 26,
		),
		$client->messageEntityBotCommand(
			offset : 67,
			length : 24,
		),
		$client->messageEntityUrl(
			offset : 17,
			length : 17,
		),
		$client->messageEntityEmail(
			offset : 48,
			length : 45,
		),
		$client->messageEntityBold(
			offset : 54,
			length : 7,
		),
		$client->messageEntityItalic(
			offset : 44,
			length : 75,
		),
		$client->messageEntityCode(
			offset : 95,
			length : 37,
		),
		$client->messageEntityPre(
			offset : 80,
			length : 29,
			language : 'tYzOAfKWeJaVTiFZ',
		),
		$client->messageEntityTextUrl(
			offset : 86,
			length : 92,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 20,
			length : 73,
			user_id : -5132332109875244267,
		),
		$client->inputMessageEntityMentionName(
			offset : 56,
			length : 98,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 91,
			length : 41,
		),
		$client->messageEntityCashtag(
			offset : 98,
			length : 92,
		),
		$client->messageEntityUnderline(
			offset : 43,
			length : 99,
		),
		$client->messageEntityStrike(
			offset : 57,
			length : 26,
		),
		$client->messageEntityBankCard(
			offset : 17,
			length : 25,
		),
		$client->messageEntitySpoiler(
			offset : 53,
			length : 97,
		),
		$client->messageEntityCustomEmoji(
			offset : 55,
			length : 58,
			document_id : 1233133095961620924,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 75,
			length : 100,
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
					user_id : -4928149670632332682,
					access_hash : 4672226279934935884,
				),
				$client->inputUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 96,
					user_id : 4136482818361181465,
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
					user_id : 5049514185803452994,
					access_hash : 8120524298074610810,
				),
				$client->inputUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 59,
					user_id : -3229258098347674066,
				),
			),
		),
		$client->inputPrivacyValueAllowChatParticipants(
			chats : array(2607008549251070831),
		),
		$client->inputPrivacyValueDisallowChatParticipants(
			chats : array(2092947522949585224),
		),
		$client->inputPrivacyValueAllowCloseFriends(),
		$client->inputPrivacyValueAllowPremium(),
		$client->inputPrivacyValueAllowBots(),
		$client->inputPrivacyValueDisallowBots(),
	),
);
```