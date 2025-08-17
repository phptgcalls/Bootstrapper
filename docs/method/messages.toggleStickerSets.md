# messages.toggleStickerSets

**Description** : *Apply changes to multiple stickersets*

**Layer** : 211

```tl
messages.toggleStickerSets#b5052fea flags:# uninstall:flags.0?true archive:flags.1?true unarchive:flags.2?true stickersets:Vector<InputStickerSet> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **uninstall** | [`flags.0?true`](type/true) | Uninstall the specified stickersets |
| **archive** | [`flags.1?true`](type/true) | Archive the specified stickersets |
| **unarchive** | [`flags.2?true`](type/true) | Unarchive the specified stickersets |
| <mark>stickersets</mark> | [`Vector<InputStickerSet>`](type/InputStickerSet) | Stickersets to act upon |

---

## Result

[Bool](type/Bool)

---

## Example

```php
$bool = $client->messages->toggleStickerSets(
	uninstall : true,
	archive : true,
	unarchive : true,
	stickersets : array(
		$client->inputStickerSetEmpty(),
		$client->inputStickerSetID(
			id : 8485537758069253902,
			access_hash : -362938022015266289,
		),
		$client->inputStickerSetShortName(
			short_name : 'y8qTcS2soO14v3RM',
		),
		$client->inputStickerSetAnimatedEmoji(),
		$client->inputStickerSetDice(
			emoticon : '3uXf1jgRZo2W0AVp',
		),
		$client->inputStickerSetAnimatedEmojiAnimations(),
		$client->inputStickerSetPremiumGifts(),
		$client->inputStickerSetEmojiGenericAnimations(),
		$client->inputStickerSetEmojiDefaultStatuses(),
		$client->inputStickerSetEmojiDefaultTopicIcons(),
		$client->inputStickerSetEmojiChannelDefaultStatuses(),
		$client->inputStickerSetTonGifts(),
	),
);
```