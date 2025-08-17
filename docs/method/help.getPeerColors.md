# help.getPeerColors

**Description** : *Get the set of accent color palettes » that can be used for message accents*

**Layer** : 211

```tl
help.getPeerColors#da80f42f hash:int = help.PeerColors;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`int`](type/int) | Hash used for caching, for more info click here |

---

## Result

[help.PeerColors](type/help.PeerColors)

---

## Example

```php
$helpPeerColors = $client->help->getPeerColors(
	hash : 78,
);
```