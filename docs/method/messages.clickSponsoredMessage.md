# messages.clickSponsoredMessage

**Description** : *Informs the server that the user has interacted with a sponsored message in one of the ways listed here »*

**Layer** : 211

```tl
messages.clickSponsoredMessage#8235057e flags:# media:flags.0?true fullscreen:flags.1?true random_id:bytes = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **media** | [`flags.0?true`](type/true) | The user clicked on the media |
| **fullscreen** | [`flags.1?true`](type/true) | The user expanded the video to full screen, and then clicked on it |
| <mark>random_id</mark> | [`bytes`](type/bytes) | The ad's unique ID |

---

## Result

[Bool](type/Bool)

---

## Example

```php
$bool = $client->messages->clickSponsoredMessage(
	media : true,
	fullscreen : true,
	random_id : '4"3XLiveProto?r?}',
);
```