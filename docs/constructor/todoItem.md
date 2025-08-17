# todoItem

**Layer** : 211

```tl
todoItem#cba9a52f id:int title:TextWithEntities = TodoItem;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`int`](type/int) | NOTHING |
| <mark>title</mark> | [`TextWithEntities`](type/TextWithEntities) | NOTHING |

---

## Type

[TodoItem](type/TodoItem)

---

## Example

```php
$todoItem = $client->todoItem(
	id : 51,
	title : $client->textWithEntities(
		text : 'nb0y1r4iQp9WjN6u',
		entities : array(
			$client->messageEntityUnknown(
				offset : 12,
				length : 66,
			),
			$client->messageEntityMention(
				offset : 23,
				length : 29,
			),
			$client->messageEntityHashtag(
				offset : 65,
				length : 10,
			),
			$client->messageEntityBotCommand(
				offset : 79,
				length : 71,
			),
			$client->messageEntityUrl(
				offset : 75,
				length : 12,
			),
			$client->messageEntityEmail(
				offset : 82,
				length : 33,
			),
			$client->messageEntityBold(
				offset : 18,
				length : 100,
			),
			$client->messageEntityItalic(
				offset : 9,
				length : 19,
			),
			$client->messageEntityCode(
				offset : 38,
				length : 75,
			),
			$client->messageEntityPre(
				offset : 99,
				length : 66,
				language : 'g5SLXwZIhau1ANE0',
			),
			$client->messageEntityTextUrl(
				offset : 82,
				length : 94,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 81,
				length : 63,
				user_id : -7345400831855377800,
			),
			$client->inputMessageEntityMentionName(
				offset : 58,
				length : 20,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 97,
				length : 6,
			),
			$client->messageEntityCashtag(
				offset : 85,
				length : 88,
			),
			$client->messageEntityUnderline(
				offset : 84,
				length : 88,
			),
			$client->messageEntityStrike(
				offset : 68,
				length : 33,
			),
			$client->messageEntityBankCard(
				offset : 74,
				length : 36,
			),
			$client->messageEntitySpoiler(
				offset : 26,
				length : 42,
			),
			$client->messageEntityCustomEmoji(
				offset : 2,
				length : 15,
				document_id : 5895979718319503025,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 25,
				length : 40,
			),
		),
	),
);
```