# messageMediaDice

**Description** : *Dice-based animated sticker*

**Layer** : 211

```tl
messageMediaDice#3f7ee58b value:int emoticon:string = MessageMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>value</mark> | [`int`](type/int) | Dice value |
| <mark>emoticon</mark> | [`string`](type/string) | The emoji, for now ,  and  are supported |

---

## Type

[MessageMedia](type/MessageMedia)

---

## Example

```php
$messageMedia = $client->messageMediaDice(
	value : 42,
	emoticon : 'mK7acZ8VFpidLB0w',
);
```