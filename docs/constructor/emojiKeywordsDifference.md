# emojiKeywordsDifference

**Description** : *Changes to emoji keywords*

**Layer** : 211

```tl
emojiKeywordsDifference#5cc761bd lang_code:string from_version:int version:int keywords:Vector<EmojiKeyword> = EmojiKeywordsDifference;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>lang_code</mark> | [`string`](type/string) | Language code for keywords |
| <mark>from_version</mark> | [`int`](type/int) | Previous emoji keyword list version |
| <mark>version</mark> | [`int`](type/int) | Current version of emoji keyword list |
| <mark>keywords</mark> | [`Vector<EmojiKeyword>`](type/EmojiKeyword) | Emojis associated to keywords |

---

## Type

[EmojiKeywordsDifference](type/EmojiKeywordsDifference)

---

## Example

```php
$emojiKeywordsDifference = $client->emojiKeywordsDifference(
	lang_code : 'BiZNa6PRnDto7ywG',
	from_version : 48,
	version : 22,
	keywords : array(
		$client->emojiKeyword(
			keyword : 'upwFcD1xmY3LMtTA',
			emoticons : array('Vs83xheOrz1l7kd6'),
		),
		$client->emojiKeywordDeleted(
			keyword : 't4Q5EHevBlRdCYsm',
			emoticons : array('Lv3pRuf4kogWmwIc'),
		),
	),
);
```