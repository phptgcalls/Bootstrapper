# messages.emojiGroups

**Description** : *Represents a list of emoji categories*

**Layer** : 211

```tl
messages.emojiGroups#881fb94b hash:int groups:Vector<EmojiGroup> = messages.EmojiGroups;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`int`](type/int) | Hash used for caching, for more info click here |
| <mark>groups</mark> | [`Vector<EmojiGroup>`](type/EmojiGroup) | A list of emoji categories |

---

## Type

[messages.EmojiGroups](type/messages.EmojiGroups)

---

## Example

```php
$messagesEmojiGroups = $client->messages->emojiGroups(
	hash : 13,
	groups : array(
		$client->emojiGroup(
			title : 'ja3qB8Fr2sIpwCUm',
			icon_emoji_id : -4171953290379364821,
			emoticons : array('rcK5ig6hMTC03Zes'),
		),
		$client->emojiGroupGreeting(
			title : 'cjhJD06lwiRSEOeI',
			icon_emoji_id : -6680602918004490238,
			emoticons : array('y1mJQE6RHLGCU3rM'),
		),
		$client->emojiGroupPremium(
			title : 'aUhCQSY9r3OlxnAi',
			icon_emoji_id : 6455906226224954207,
		),
	),
);
```