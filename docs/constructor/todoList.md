# todoList

**Layer** : 211

```tl
todoList#49b92a26 flags:# others_can_append:flags.0?true others_can_complete:flags.1?true title:TextWithEntities list:Vector<TodoItem> = TodoList;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **others_can_append** | [`flags.0?true`](type/true) | NOTHING |
| **others_can_complete** | [`flags.1?true`](type/true) | NOTHING |
| <mark>title</mark> | [`TextWithEntities`](type/TextWithEntities) | NOTHING |
| <mark>list</mark> | [`Vector<TodoItem>`](type/TodoItem) | NOTHING |

---

## Type

[TodoList](type/TodoList)

---

## Example

```php
$todoList = $client->todoList(
	others_can_append : true,
	others_can_complete : true,
	title : $client->textWithEntities(
		text : 'uKmlTt8IxENaqgvo',
		entities : array(
			$client->messageEntityUnknown(
				offset : 43,
				length : 5,
			),
			$client->messageEntityMention(
				offset : 89,
				length : 68,
			),
			$client->messageEntityHashtag(
				offset : 50,
				length : 41,
			),
			$client->messageEntityBotCommand(
				offset : 81,
				length : 43,
			),
			$client->messageEntityUrl(
				offset : 11,
				length : 99,
			),
			$client->messageEntityEmail(
				offset : 52,
				length : 34,
			),
			$client->messageEntityBold(
				offset : 42,
				length : 53,
			),
			$client->messageEntityItalic(
				offset : 43,
				length : 38,
			),
			$client->messageEntityCode(
				offset : 49,
				length : 37,
			),
			$client->messageEntityPre(
				offset : 41,
				length : 12,
				language : 'MJznWik9g8xYFrXm',
			),
			$client->messageEntityTextUrl(
				offset : 54,
				length : 2,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 23,
				length : 1,
				user_id : 5375910756162749723,
			),
			$client->inputMessageEntityMentionName(
				offset : 82,
				length : 40,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 61,
				length : 59,
			),
			$client->messageEntityCashtag(
				offset : 67,
				length : 39,
			),
			$client->messageEntityUnderline(
				offset : 10,
				length : 56,
			),
			$client->messageEntityStrike(
				offset : 23,
				length : 68,
			),
			$client->messageEntityBankCard(
				offset : 64,
				length : 38,
			),
			$client->messageEntitySpoiler(
				offset : 27,
				length : 52,
			),
			$client->messageEntityCustomEmoji(
				offset : 44,
				length : 16,
				document_id : -4081324740101568630,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 3,
				length : 67,
			),
		),
	),
	list : array(
		$client->todoItem(
			id : 98,
			title : $client->textWithEntities(
				text : '8XRot1Y02GENZ6UJ',
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
		),
	),
);
```