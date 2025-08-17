# messages.reactions

**Description** : *List of message reactions*

**Layer** : 211

```tl
messages.reactions#eafdf716 hash:long reactions:Vector<Reaction> = messages.Reactions;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>reactions</mark> | [`Vector<Reaction>`](type/Reaction) | Reactions |

---

## Type

[messages.Reactions](type/messages.Reactions)

---

## Example

```php
$messagesReactions = $client->messages->reactions(
	hash : -2506625778397959895,
	reactions : array(
		$client->reactionEmpty(),
		$client->reactionEmoji(
			emoticon : 'XzbCrU3YspJEFmoG',
		),
		$client->reactionCustomEmoji(
			document_id : 8724923321794447768,
		),
		$client->reactionPaid(),
	),
);
```