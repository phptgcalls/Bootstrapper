# inputMediaPoll

**Description** : *A poll*

**Layer** : 211

```tl
inputMediaPoll#f94e5f1 flags:# poll:Poll correct_answers:flags.0?Vector<bytes> solution:flags.1?string solution_entities:flags.1?Vector<MessageEntity> = InputMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>poll</mark> | [`Poll`](type/Poll) | The poll to send |
| **correct_answers** | [`flags.0?Vector<bytes>`](type/bytes) | Correct answer IDs (for quiz polls) |
| **solution** | [`flags.1?string`](type/string) | Explanation of quiz solution |
| **solution_entities** | [`flags.1?Vector<MessageEntity>`](type/MessageEntity) | Message entities for styled text |

---

## Type

[InputMedia](type/InputMedia)

---

## Example

```php
$inputMedia = $client->inputMediaPoll(
	poll : $client->poll(
		id : 5847652744398976201,
		closed : true,
		public_voters : true,
		multiple_choice : true,
		quiz : true,
		question : $client->textWithEntities(
			text : 'vmRxeSoGLPcFwUTf',
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
				option : '<??(?LiveProtoNMӨ',
			),
		),
		close_period : 80,
		close_date : 48,
	),
	correct_answers : array('?p??LiveProto>????'),
	solution : '7dN1lJasPto0CMFZ',
	solution_entities : array(
		$client->messageEntityUnknown(
			offset : 73,
			length : 51,
		),
		$client->messageEntityMention(
			offset : 98,
			length : 78,
		),
		$client->messageEntityHashtag(
			offset : 74,
			length : 22,
		),
		$client->messageEntityBotCommand(
			offset : 83,
			length : 69,
		),
		$client->messageEntityUrl(
			offset : 47,
			length : 3,
		),
		$client->messageEntityEmail(
			offset : 40,
			length : 30,
		),
		$client->messageEntityBold(
			offset : 90,
			length : 0,
		),
		$client->messageEntityItalic(
			offset : 53,
			length : 80,
		),
		$client->messageEntityCode(
			offset : 53,
			length : 69,
		),
		$client->messageEntityPre(
			offset : 65,
			length : 90,
			language : '5BljOKeuMPfvnHqo',
		),
		$client->messageEntityTextUrl(
			offset : 9,
			length : 58,
			url : 'https://docs.liveproto.dev',
		),
		$client->messageEntityMentionName(
			offset : 76,
			length : 34,
			user_id : -4473273956598200429,
		),
		$client->inputMessageEntityMentionName(
			offset : 1,
			length : 7,
			user_id : $client->inputUserEmpty(),
		),
		$client->messageEntityPhone(
			offset : 26,
			length : 11,
		),
		$client->messageEntityCashtag(
			offset : 18,
			length : 34,
		),
		$client->messageEntityUnderline(
			offset : 16,
			length : 47,
		),
		$client->messageEntityStrike(
			offset : 10,
			length : 74,
		),
		$client->messageEntityBankCard(
			offset : 58,
			length : 92,
		),
		$client->messageEntitySpoiler(
			offset : 69,
			length : 2,
		),
		$client->messageEntityCustomEmoji(
			offset : 85,
			length : 13,
			document_id : -3792906133366732807,
		),
		$client->messageEntityBlockquote(
			collapsed : true,
			offset : 41,
			length : 58,
		),
	),
);
```