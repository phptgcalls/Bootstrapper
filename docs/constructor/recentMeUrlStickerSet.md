# recentMeUrlStickerSet

**Description** : *Recent t.me stickerset installation URL*

**Layer** : 211

```tl
recentMeUrlStickerSet#bc0a57dc url:string set:StickerSetCovered = RecentMeUrl;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>url</mark> | [`string`](type/string) | t.me URL |
| <mark>set</mark> | [`StickerSetCovered`](type/StickerSetCovered) | Stickerset |

---

## Type

[RecentMeUrl](type/RecentMeUrl)

---

## Example

```php
$recentMeUrl = $client->recentMeUrlStickerSet(
	url : 'https://docs.liveproto.dev',
	set : $client->stickerSetCovered(
		set : $client->stickerSet(
			archived : true,
			official : true,
			masks : true,
			emojis : true,
			text_color : true,
			channel_emoji_status : true,
			creator : true,
			installed_date : 41,
			id : 7169655074501017946,
			access_hash : -6106942682117025598,
			title : 'IyEDCfuKr1waOdsU',
			short_name : 'XSn8o9hy14QOlIqL',
			thumbs : array(
				$client->photoSizeEmpty(...),
				$client->photoSize(...),
				$client->photoCachedSize(...),
				$client->photoStrippedSize(...),
				$client->photoSizeProgressive(...),
				$client->photoPathSize(...),
			),
			thumb_dc_id : 56,
			thumb_version : 20,
			thumb_document_id : 3624406021527112939,
			count : 88,
			hash : 53,
		),
		cover : $client->documentEmpty(
			id : -6193058841275362191,
		),
	),
);
```