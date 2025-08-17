# messages.getAttachMenuBots

**Description** : *Returns installed attachment menu bot mini apps »*

**Layer** : 211

```tl
messages.getAttachMenuBots#16fcc2cb hash:long = AttachMenuBots;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |

---

## Result

[AttachMenuBots](type/AttachMenuBots)

---

## Example

```php
$attachMenuBots = $client->messages->getAttachMenuBots(
	hash : -2329384351623832036,
);
```