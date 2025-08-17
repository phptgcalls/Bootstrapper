# messages.getEmojiKeywordsLanguages

**Description** : *Obtain a list of related languages that must be used when fetching emoji keyword lists »*

**Layer** : 211

```tl
messages.getEmojiKeywordsLanguages#4e9963b2 lang_codes:Vector<string> = Vector<EmojiLanguage>;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>lang_codes</mark> | [`Vector<string>`](type/string) | The user's language codes |

---

## Result

[Vector<EmojiLanguage>](type/EmojiLanguage)

---

## Example

```php
$emojiLanguage = $client->messages->getEmojiKeywordsLanguages(
	lang_codes : array('7Q1yP2wbhdqgpxlo'),
);
```