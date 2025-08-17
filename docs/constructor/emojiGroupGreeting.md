# emojiGroupGreeting

**Description** : *Represents an emoji category, that should be moved to the top of the list when choosing a sticker for a business introduction*

**Layer** : 211

```tl
emojiGroupGreeting#80d26cc7 title:string icon_emoji_id:long emoticons:Vector<string> = EmojiGroup;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>title</mark> | [`string`](type/string) | Category name, i.e. "Animals", "Flags", "Faces" and so on |
| <mark>icon_emoji_id</mark> | [`long`](type/long) | A single custom emoji used as preview for the category |
| <mark>emoticons</mark> | [`Vector<string>`](type/string) | A list of UTF-8 emojis, matching the category |

---

## Type

[EmojiGroup](type/EmojiGroup)

---

## Example

```php
$emojiGroup = $client->emojiGroupGreeting(
	title : '5qwEFSTJG9eun81c',
	icon_emoji_id : -2539925217570450252,
	emoticons : array('y9bn28RELl13N40g'),
);
```