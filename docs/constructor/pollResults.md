# pollResults

**Description** : *Results of poll*

**Layer** : 211

```tl
pollResults#7adf2420 flags:# min:flags.0?true results:flags.1?Vector<PollAnswerVoters> total_voters:flags.2?int recent_voters:flags.3?Vector<Peer> solution:flags.4?string solution_entities:flags.4?Vector<MessageEntity> = PollResults;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **min** | [`flags.0?true`](type/true) | Similar to min objects, used for poll constructors that are the same for all users so they don't have the option chosen by the current user (you can use messages.getPollResults to get the full poll results) |
| **results** | [`flags.1?Vector<PollAnswerVoters>`](type/PollAnswerVoters) | Poll results |
| **total_voters** | [`flags.2?int`](type/int) | Total number of people that voted in the poll |
| **recent_voters** | [`flags.3?Vector<Peer>`](type/Peer) | IDs of the last users that recently voted in the poll |
| **solution** | [`flags.4?string`](type/string) | Explanation of quiz solution |
| **solution_entities** | [`flags.4?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text in quiz solution |

---

## Type

[PollResults](type/PollResults)

---

## Example

```php
$pollResults = $client->pollResults(
	min : true,
	results : array(
		$client->pollAnswerVoters(
			chosen : true,
			correct : true,
			option : '??=?LiveProto??b',
			voters : 44,
		),
	),
	total_voters : 70,
	recent_voters : array(
		$client->peerUser(
			user_id : -8807536351116165018,
		),
		$client->peerChat(
			chat_id : -7536761044670248999,
		),
		$client->peerChannel(
			channel_id : 4416165549889150071,
		),
	),
	solution : 'sA93VTfdUIWwYJL6',
	solution_entities : array(
		$client->messageEntityUnknown(
			offset : 81,
			length : 41,
		),
		$client->messageEntityMention(
			offset : 50,
			length : 59,
		),
		$client->messageEntityHashtag(
			offset : 24,
			length : 72,
		),
		$client->messageEntityBotCommand(
			offset : 61,
			length : 41,
		),
		$client->messageEntityUrl(
			offset : 11,
			length : 47,
		),
		$client->messageEntityEmail(
			offset : 86,
			length : 11,
		),
		$client->messageEntityBold(
			offset : 64,
			length : 72,
		),
		$client->messageEntityItalic(
			offset : 85,
			length : 16,
		),
		$client->messageEntityCode(
			offset : 67,
			length : 19,
		),
		$client->messageEntityPre(
			offset : 69,
			length : 60,
			language : 'Kyto98fBZcbizajU',
		),
		$client->messageEntityTextUrl(
			offset : 72,
			length : 25,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 41,
			length : 96,
			user_id : 4173119305253103045,
		),
		$client->inputMessageEntityMentionName(
			offset : 82,
			length : 43,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 24,
			length : 25,
		),
		$client->messageEntityCashtag(
			offset : 31,
			length : 13,
		),
		$client->messageEntityUnderline(
			offset : 59,
			length : 51,
		),
		$client->messageEntityStrike(
			offset : 35,
			length : 7,
		),
		$client->messageEntityBankCard(
			offset : 8,
			length : 32,
		),
		$client->messageEntitySpoiler(
			offset : 96,
			length : 100,
		),
		$client->messageEntityCustomEmoji(
			offset : 65,
			length : 50,
			document_id : 4369253792562017792,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 49,
			length : 55,
		),
	),
);
```