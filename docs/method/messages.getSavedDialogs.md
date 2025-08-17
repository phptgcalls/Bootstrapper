# messages.getSavedDialogs

**Description** : *Returns the current saved dialog list, see here » for more info*

**Layer** : 211

```tl
messages.getSavedDialogs#1e91fc99 flags:# exclude_pinned:flags.0?true parent_peer:flags.1?InputPeer offset_date:int offset_id:int offset_peer:InputPeer limit:int hash:long = messages.SavedDialogs;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **exclude_pinned** | [`flags.0?true`](type/true) | Exclude pinned dialogs |
| **parent_peer** | [`flags.1?InputPeer`](type/InputPeer) | NOTHING |
| <mark>offset_date</mark> | [`int`](type/int) | Offsets for pagination, for more info click here |
| <mark>offset_id</mark> | [`int`](type/int) | Offsets for pagination, for more info click here (top_message ID used for pagination) |
| <mark>offset_peer</mark> | [`InputPeer`](type/InputPeer) | Offset peer for pagination |
| <mark>limit</mark> | [`int`](type/int) | Number of list elements to be returned |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Result

[messages.SavedDialogs](type/messages.SavedDialogs)

---

## Example

```php
$messagesSavedDialogs = $client->messages->getSavedDialogs(
	exclude_pinned : true,
	parent_peer : $client->inputPeerEmpty(),
	offset_date : 33,
	offset_id : 27,
	offset_peer : $client->inputPeerEmpty(),
	limit : 35,
	hash : 8850824484125824293,
);
```