# messages.getQuickReplyMessages

**Description** : *Fetch (a subset or all) messages in a quick reply shortcut »*

**Layer** : 211

```tl
messages.getQuickReplyMessages#94a495c3 flags:# shortcut_id:int id:flags.0?Vector<int> hash:long = messages.Messages;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>shortcut_id</mark> | [`int`](type/int) | Quick reply shortcut ID |
| **id** | [`flags.0?Vector<int>`](type/int) | IDs of the messages to fetch, if empty fetches all of them |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Result

[messages.Messages](type/messages.Messages)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **SHORTCUT_INVALID** | `400` | The specified shortcut is invalid |

---

## Example

```php
$messagesMessages = $client->messages->getQuickReplyMessages(
	shortcut_id : 37,
	id : array(0),
	hash : -6836650188153254161,
);
```