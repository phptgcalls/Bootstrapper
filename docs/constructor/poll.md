# poll

**Description** : *Poll*

**Layer** : 211

```tl
poll#58747131 id:long flags:# closed:flags.0?true public_voters:flags.1?true multiple_choice:flags.2?true quiz:flags.3?true question:TextWithEntities answers:Vector<PollAnswer> close_period:flags.4?int close_date:flags.5?int = Poll;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | ID of the poll |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **closed** | [`flags.0?true`](type/true) | Whether the poll is closed and doesn't accept any more answers |
| **public_voters** | [`flags.1?true`](type/true) | Whether cast votes are publicly visible to all users (non-anonymous poll) |
| **multiple_choice** | [`flags.2?true`](type/true) | Whether multiple options can be chosen as answer |
| **quiz** | [`flags.3?true`](type/true) | Whether this is a quiz (with wrong and correct answers, results shown in the return type) |
| <mark>question</mark> | [`TextWithEntities`](type/TextWithEntities) | The question of the poll (only Premium users can use custom emoji entities here) |
| <mark>answers</mark> | [`Vector<PollAnswer>`](type/PollAnswer) | The possible answers, vote using messages.sendVote |
| **close_period** | [`flags.4?int`](type/int) | Amount of time in seconds the poll will be active after creation, 5-600. Can't be used together with close_date |
| **close_date** | [`flags.5?int`](type/int) | Point in time (Unix timestamp) when the poll will be automatically closed. Must be at least 5 and no more than 600 seconds in the future; can't be used together with close_period |

---

## Type

[Poll](type/Poll)

---

## Example

```php
$poll = $client->poll(
	id : 8744966541281170629,
	closed : true,
	public_voters : true,
	multiple_choice : true,
	quiz : true,
	question : $client->textWithEntities(
		text : 'wZiqecasrQ0EuV34',
		entities : array(
			$client->messageEntityUnknown(
				offset : 53,
				length : 64,
			),
			$client->messageEntityMention(
				offset : 14,
				length : 53,
			),
			$client->messageEntityHashtag(
				offset : 53,
				length : 23,
			),
			$client->messageEntityBotCommand(
				offset : 52,
				length : 17,
			),
			$client->messageEntityUrl(
				offset : 15,
				length : 27,
			),
			$client->messageEntityEmail(
				offset : 81,
				length : 55,
			),
			$client->messageEntityBold(
				offset : 26,
				length : 36,
			),
			$client->messageEntityItalic(
				offset : 24,
				length : 56,
			),
			$client->messageEntityCode(
				offset : 93,
				length : 95,
			),
			$client->messageEntityPre(
				offset : 62,
				length : 68,
				language : 'LgCBVPiMauU5GvWR',
			),
			$client->messageEntityTextUrl(
				offset : 27,
				length : 75,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 91,
				length : 61,
				user_id : 7462911617294245241,
			),
			$client->inputMessageEntityMentionName(
				offset : 99,
				length : 21,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 81,
				length : 18,
			),
			$client->messageEntityCashtag(
				offset : 54,
				length : 12,
			),
			$client->messageEntityUnderline(
				offset : 98,
				length : 42,
			),
			$client->messageEntityStrike(
				offset : 45,
				length : 75,
			),
			$client->messageEntityBankCard(
				offset : 55,
				length : 7,
			),
			$client->messageEntitySpoiler(
				offset : 12,
				length : 23,
			),
			$client->messageEntityCustomEmoji(
				offset : 85,
				length : 62,
				document_id : -4687227009915816521,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 17,
				length : 14,
			),
		),
	),
	answers : array(
		$client->pollAnswer(
			text : $client->textWithEntities(
				text : 'nudm8PNCUexEl0MG',
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
			option : '??ϵLiveProto,?A',
		),
	),
	close_period : 34,
	close_date : 50,
);
```