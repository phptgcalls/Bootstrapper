# updateQuickReplies

**Description** : *Info about or the order of quick reply shortcuts » was changed*

**Layer** : 211

```tl
updateQuickReplies#f9470ab2 quick_replies:Vector<QuickReply> = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>quick_replies</mark> | [`Vector<QuickReply>`](type/QuickReply) | New quick reply shortcut order and information |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateQuickReplies(
	quick_replies : array(
		$client->quickReply(
			shortcut_id : 75,
			shortcut : '8eVEwDIAB6x9uyqJ',
			top_message : 75,
			count : 17,
		),
	),
);
```