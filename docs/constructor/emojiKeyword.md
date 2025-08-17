# emojiKeyword

**Description** : *Emoji keyword*

**Layer** : 211

```tl
emojiKeyword#d5b3b9f9 keyword:string emoticons:Vector<string> = EmojiKeyword;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>keyword</mark> | [`string`](type/string) | Keyword |
| <mark>emoticons</mark> | [`Vector<string>`](type/string) | Emojis associated to keyword |

---

## Type

[EmojiKeyword](type/EmojiKeyword)

---

## Example

```php
$emojiKeyword = $client->emojiKeyword(
	keyword : 'PwDjhpGRLecaBUA8',
	emoticons : array('oeFmOq0ZtXi4QBgG'),
);
```