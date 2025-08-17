# updateMessagePoll

**Description** : *The results of a poll have changed*

**Layer** : 211

```tl
updateMessagePoll#aca1657b flags:# poll_id:long poll:flags.0?Poll results:PollResults = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>poll_id</mark> | [`long`](type/long) | Poll ID |
| **poll** | [`flags.0?Poll`](type/Poll) | If the server knows the client hasn't cached this poll yet, the poll itself |
| <mark>results</mark> | [`PollResults`](type/PollResults) | New poll results |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateMessagePoll(
	poll_id : -2136111329020523018,
	poll : $client->poll(
		id : -8522468983267160335,
		closed : true,
		public_voters : true,
		multiple_choice : true,
		quiz : true,
		question : $client->textWithEntities(
			text : 'wAMskYcPadDWpZLV',
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
				option : '?ޣ;LiveProto?A??!',
			),
		),
		close_period : 51,
		close_date : 78,
	),
	results : $client->pollResults(
		min : true,
		results : array(
			$client->pollAnswerVoters(
				chosen : true,
				correct : true,
				option : 'tsU?LiveProto=?I?',
				voters : 62,
			),
		),
		total_voters : 36,
		recent_voters : array(
			$client->peerUser(
				user_id : -1981098545876110091,
			),
			$client->peerChat(
				chat_id : 3128201566587180433,
			),
			$client->peerChannel(
				channel_id : -5798404649679121615,
			),
		),
		solution : 'xz0QjCDH1L2K3oMG',
		solution_entities : array(
			$client->messageEntityUnknown(
				offset : 74,
				length : 43,
			),
			$client->messageEntityMention(
				offset : 73,
				length : 12,
			),
			$client->messageEntityHashtag(
				offset : 62,
				length : 43,
			),
			$client->messageEntityBotCommand(
				offset : 63,
				length : 7,
			),
			$client->messageEntityUrl(
				offset : 96,
				length : 73,
			),
			$client->messageEntityEmail(
				offset : 55,
				length : 68,
			),
			$client->messageEntityBold(
				offset : 91,
				length : 50,
			),
			$client->messageEntityItalic(
				offset : 89,
				length : 83,
			),
			$client->messageEntityCode(
				offset : 36,
				length : 93,
			),
			$client->messageEntityPre(
				offset : 4,
				length : 32,
				language : 'JBKpuIYiCNgDm54o',
			),
			$client->messageEntityTextUrl(
				offset : 74,
				length : 22,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 65,
				length : 25,
				user_id : -6247739290298913274,
			),
			$client->inputMessageEntityMentionName(
				offset : 79,
				length : 88,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 45,
				length : 94,
			),
			$client->messageEntityCashtag(
				offset : 98,
				length : 76,
			),
			$client->messageEntityUnderline(
				offset : 90,
				length : 40,
			),
			$client->messageEntityStrike(
				offset : 53,
				length : 3,
			),
			$client->messageEntityBankCard(
				offset : 77,
				length : 63,
			),
			$client->messageEntitySpoiler(
				offset : 25,
				length : 89,
			),
			$client->messageEntityCustomEmoji(
				offset : 56,
				length : 63,
				document_id : -5487276075452073376,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 72,
				length : 22,
			),
		),
	),
);
```