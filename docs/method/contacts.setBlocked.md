# contacts.setBlocked

**Description** : *Replace the contents of an entire blocklist, see here for more info »*

**Layer** : 211

```tl
contacts.setBlocked#94c65c76 flags:# my_stories_from:flags.0?true id:Vector<InputPeer> limit:int = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **my_stories_from** | [`flags.0?true`](type/true) | Whether to edit the story blocklist; if not set, will edit the main blocklist. See here » for differences between the two |
| <mark>id</mark> | [`Vector<InputPeer>`](type/InputPeer) | Full content of the blocklist |
| <mark>limit</mark> | [`int`](type/int) | Maximum number of results to return, see pagination |

---

## Result

[Bool](type/Bool)

---

## Example

```php
$bool = $client->contacts->setBlocked(
	my_stories_from : true,
	id : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : 8454222882558932564,
		),
		$client->inputPeerUser(
			user_id : -5676837446734865872,
			access_hash : -2412297582473975401,
		),
		$client->inputPeerChannel(
			channel_id : 5476048630633133864,
			access_hash : 6870824761900845486,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 91,
			user_id : 1207185243642420140,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 68,
			channel_id : 7113696056563054201,
		),
	),
	limit : 56,
);
```