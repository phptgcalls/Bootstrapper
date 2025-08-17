# messageActionSetChatWallPaper

**Description** : *The wallpaper » of the current chat was changed*

**Layer** : 211

```tl
messageActionSetChatWallPaper#5060a3f4 flags:# same:flags.0?true for_both:flags.1?true wallpaper:WallPaper = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **same** | [`flags.0?true`](type/true) | If set, indicates the user applied a wallpaper » previously sent by the other user in a messageActionSetChatWallPaper message |
| **for_both** | [`flags.1?true`](type/true) | If set, indicates the wallpaper was forcefully applied for both sides, without explicit confirmation from the other side. If the message is incoming, and we did not like the new wallpaper the other user has chosen for us, we can re-set our previous wallpaper just on our side, by invoking messages.setChatWallPaper, providing only the revert flag (and obviously the peer parameter) |
| <mark>wallpaper</mark> | [`WallPaper`](type/WallPaper) | New wallpaper |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionSetChatWallPaper(
	same : true,
	for_both : true,
	wallpaper : $client->wallPaper(
		id : 3642336270073564010,
		creator : true,
		default : true,
		pattern : true,
		dark : true,
		access_hash : 2987368097513790543,
		slug : '461BLOqJdyRVoXre',
		document : $client->documentEmpty(
			id : 7402097512005902104,
		),
		settings : $client->wallPaperSettings(
			blur : true,
			motion : true,
			background_color : 53,
			second_background_color : 38,
			third_background_color : 76,
			fourth_background_color : 63,
			intensity : 93,
			rotation : 100,
			emoticon : '40Dglyu9aA7KoN6H',
		),
	),
);
```