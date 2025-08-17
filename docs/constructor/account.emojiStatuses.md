# account.emojiStatuses

**Description** : *A list of emoji statuses*

**Layer** : 211

```tl
account.emojiStatuses#90c467d1 hash:long statuses:Vector<EmojiStatus> = account.EmojiStatuses;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>statuses</mark> | [`Vector<EmojiStatus>`](type/EmojiStatus) | Emoji statuses |

---

## Type

[account.EmojiStatuses](type/account.EmojiStatuses)

---

## Example

```php
$accountEmojiStatuses = $client->account->emojiStatuses(
	hash : 546436681673478646,
	statuses : array(
		$client->emojiStatusEmpty(),
		$client->emojiStatus(
			document_id : 4546926975158666780,
			until : 16,
		),
		$client->emojiStatusCollectible(
			collectible_id : -1181783801327086278,
			document_id : -4233261082395978036,
			title : 'AbHLiqkdJwmyg2eX',
			slug : 'ULYDueBWTnv43oPA',
			pattern_document_id : 1489047188611919946,
			center_color : 93,
			edge_color : 97,
			pattern_color : 25,
			text_color : 83,
			until : 55,
		),
		$client->inputEmojiStatusCollectible(
			collectible_id : -3862332024983010734,
			until : 58,
		),
	),
);
```