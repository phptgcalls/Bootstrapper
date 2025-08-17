# webPageAttributeStarGiftCollection

**Layer** : 211

```tl
webPageAttributeStarGiftCollection#31cad303 icons:Vector<Document> = WebPageAttribute;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>icons</mark> | [`Vector<Document>`](type/Document) | NOTHING |

---

## Type

[WebPageAttribute](type/WebPageAttribute)

---

## Example

```php
$webPageAttribute = $client->webPageAttributeStarGiftCollection(
	icons : array(
		$client->documentEmpty(
			id : 4926847620664636674,
		),
		$client->document(
			id : 8106339457972698700,
			access_hash : -2252804692153934324,
			file_reference : '??7?LiveProto??^??',
			date : 83,
			mime_type : '0hKdkmM1cGfRznST',
			size : -7104334426046322791,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'Pq8CyoSYZB4HTbjg',
				),
				$client->photoSize(
					type : 'h7XWOAMd1gC2rGej',
					w : 50,
					h : 95,
					size : 60,
				),
				$client->photoCachedSize(
					type : 'tTGbIPEoHleV9adQ',
					w : 82,
					h : 70,
					bytes : '??_?LiveProto;???',
				),
				$client->photoStrippedSize(
					type : 'mue7hPbHrwyfXSTk',
					bytes : 'E???LiveProto
???',
				),
				$client->photoSizeProgressive(
					type : 'roweTUq2AspFEuK9',
					w : 25,
					h : 27,
					sizes : array(43),
				),
				$client->photoPathSize(
					type : 'XfrCWpMhUPxcAgFi',
					bytes : ',?^bLiveProtox?H??',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'EQOG754vpBsHSJDf',
					w : 81,
					h : 57,
					size : 71,
					video_start_ts : -1598951.859375,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 6445896178403767152,
					background_colors : array(98),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : -6711238503483655467,
					background_colors : array(99),
				),
			),
			dc_id : 93,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 2,
					h : 94,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'tzanUgrdTeuJcPKX',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -1309502.8134765625,
					w : 41,
					h : 41,
					preload_prefix_size : 30,
					video_start_ts : -204283.76171875,
					video_codec : 'g1oMWtHr0vwDQX6m',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 50,
					title : 'MZG8Ri9sJtaAFOhU',
					performer : '74XLK3ujBetq6NGh',
					waveform : 'z?ӷLiveProto??A?',
				),
				$client->documentAttributeFilename(
					file_name : '7Oh4mJwfRx6CN1oe',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'DASUu6j8zLh7PXMr',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```