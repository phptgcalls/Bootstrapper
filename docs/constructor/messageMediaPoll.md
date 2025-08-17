# messageMediaPoll

**Description** : *Poll*

**Layer** : 211

```tl
messageMediaPoll#4bd6e798 poll:Poll results:PollResults = MessageMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>poll</mark> | [`Poll`](type/Poll) | The poll |
| <mark>results</mark> | [`PollResults`](type/PollResults) | The results of the poll |

---

## Type

[MessageMedia](type/MessageMedia)

---

## Example

```php
$messageMedia = $client->messageMediaPoll(
	poll : $client->poll(
		id : 7594074716461608477,
		closed : true,
		public_voters : true,
		multiple_choice : true,
		quiz : true,
		question : $client->textWithEntities(
			text : 'mpG1MXZBxUcREKrV',
			entities : array(
				$client->messageEntityUnknown(...),
				$client->messageEntityMention(...),
				$client->messageEntityHashtag(...),
				$client->messageEntityBotCommand(...),
				$client->messageEntityUrl(...),
				$client->messageEntityEmail(...),
				$client->messageEntityBold(...),
				$client->messageEntityItalic(...),
				$client->messageEntityCode(...),
				$client->messageEntityPre(...),
				$client->messageEntityTextUrl(...),
				$client->messageEntityMentionName(...),
				$client->inputMessageEntityMentionName(...),
				$client->messageEntityPhone(...),
				$client->messageEntityCashtag(...),
				$client->messageEntityUnderline(...),
				$client->messageEntityStrike(...),
				$client->messageEntityBankCard(...),
				$client->messageEntitySpoiler(...),
				$client->messageEntityCustomEmoji(...),
				$client->messageEntityBlockquote(...),
			),
		),
		answers : array(
			$client->pollAnswer(
				text : $client->textWithEntities(...),
				option : '?~_A?LiveProto' . "\0" . '?B?',
			),
		),
		close_period : 6,
		close_date : 85,
	),
	results : $client->pollResults(
		min : true,
		results : array(
			$client->pollAnswerVoters(
				chosen : true,
				correct : true,
				option : '?EhxLiveProto?fkfH',
				voters : 12,
			),
		),
		total_voters : 24,
		recent_voters : array(
			$client->peerUser(
				user_id : 2151453696176970628,
			),
			$client->peerChat(
				chat_id : 5850965678804938259,
			),
			$client->peerChannel(
				channel_id : -8300322951365215784,
			),
		),
		solution : 'pvdtVRqsaHi7JNQj',
		solution_entities : array(
			$client->messageEntityUnknown(
				offset : 2,
				length : 84,
			),
			$client->messageEntityMention(
				offset : 20,
				length : 24,
			),
			$client->messageEntityHashtag(
				offset : 36,
				length : 31,
			),
			$client->messageEntityBotCommand(
				offset : 59,
				length : 84,
			),
			$client->messageEntityUrl(
				offset : 45,
				length : 6,
			),
			$client->messageEntityEmail(
				offset : 2,
				length : 6,
			),
			$client->messageEntityBold(
				offset : 11,
				length : 82,
			),
			$client->messageEntityItalic(
				offset : 74,
				length : 60,
			),
			$client->messageEntityCode(
				offset : 92,
				length : 7,
			),
			$client->messageEntityPre(
				offset : 45,
				length : 80,
				language : 'ypF1mfBocRe3rqgJ',
			),
			$client->messageEntityTextUrl(
				offset : 19,
				length : 47,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 19,
				length : 75,
				user_id : 9097237289322300220,
			),
			$client->inputMessageEntityMentionName(
				offset : 10,
				length : 82,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 32,
				length : 91,
			),
			$client->messageEntityCashtag(
				offset : 71,
				length : 88,
			),
			$client->messageEntityUnderline(
				offset : 16,
				length : 68,
			),
			$client->messageEntityStrike(
				offset : 57,
				length : 15,
			),
			$client->messageEntityBankCard(
				offset : 76,
				length : 49,
			),
			$client->messageEntitySpoiler(
				offset : 26,
				length : 39,
			),
			$client->messageEntityCustomEmoji(
				offset : 31,
				length : 28,
				document_id : -2055067086349651119,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 41,
				length : 22,
			),
		),
	),
);
```