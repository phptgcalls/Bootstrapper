# messages.searchStickerSets

**Description** : *Search for stickersets*

**Layer** : 211

```tl
messages.searchStickerSets#35705b8a flags:# exclude_featured:flags.0?true q:string hash:long = messages.FoundStickerSets;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **exclude_featured** | [`flags.0?true`](type/true) | Exclude featured stickersets from results |
| <mark>q</mark> | [`string`](type/string) | Query string |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Result

[messages.FoundStickerSets](type/messages.FoundStickerSets)

---

## Example

```php
$messagesFoundStickerSets = $client->messages->searchStickerSets(
	exclude_featured : true,
	q : '3n7LWjRQAxabiKcF',
	hash : 5041186508525692717,
);
```