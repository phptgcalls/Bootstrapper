# messageExtendedMediaPreview

**Description** : *Paid media preview for not yet purchased paid media, see here » for more info*

**Layer** : 211

```tl
messageExtendedMediaPreview#ad628cc8 flags:# w:flags.0?int h:flags.0?int thumb:flags.1?PhotoSize video_duration:flags.2?int = MessageExtendedMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **w** | [`flags.0?int`](type/int) | Width |
| **h** | [`flags.0?int`](type/int) | Height |
| **thumb** | [`flags.1?PhotoSize`](type/PhotoSize) | Extremely low resolution thumbnail |
| **video_duration** | [`flags.2?int`](type/int) | Video duration for videos |

---

## Type

[MessageExtendedMedia](type/MessageExtendedMedia)

---

## Example

```php
$messageExtendedMedia = $client->messageExtendedMediaPreview(
	w : 40,
	h : 48,
	thumb : $client->photoSizeEmpty(
		type : '17pqFwsmbcSNTeUC',
	),
	video_duration : 91,
);
```