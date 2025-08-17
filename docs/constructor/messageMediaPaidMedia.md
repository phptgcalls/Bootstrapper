# messageMediaPaidMedia

**Description** : *Paid media, see here » for more info*

**Layer** : 211

```tl
messageMediaPaidMedia#a8852491 stars_amount:long extended_media:Vector<MessageExtendedMedia> = MessageMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>stars_amount</mark> | [`long`](type/long) | The price of the media in Telegram Stars |
| <mark>extended_media</mark> | [`Vector<MessageExtendedMedia>`](type/MessageExtendedMedia) | Either the paid-for media, or super low resolution media previews if the media wasn't purchased yet, see here » for more info |

---

## Type

[MessageMedia](type/MessageMedia)

---

## Example

```php
$messageMedia = $client->messageMediaPaidMedia(
	stars_amount : -7680778226525014316,
	extended_media : array(
		$client->messageExtendedMediaPreview(
			w : 89,
			h : 28,
			thumb : $client->photoSizeEmpty(
				type : '7FtCZo1l2SEzg3Np',
			),
			video_duration : 0,
		),
		$client->messageExtendedMedia(
			media : $client->messageMediaEmpty(),
		),
	),
);
```