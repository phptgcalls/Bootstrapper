# messages.savedGifs

**Description** : *Saved gifs*

**Layer** : 211

```tl
messages.savedGifs#84a02a0d hash:long gifs:Vector<Document> = messages.SavedGifs;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>gifs</mark> | [`Vector<Document>`](type/Document) | List of saved gifs |

---

## Type

[messages.SavedGifs](type/messages.SavedGifs)

---

## Example

```php
$messagesSavedGifs = $client->messages->savedGifs(
	hash : -8150794017936368670,
	gifs : array(
		$client->documentEmpty(
			id : 8612085204680159544,
		),
		$client->document(
			id : -6106816668588823342,
			access_hash : -1889088770456045092,
			file_reference : '.???LiveProto,??!	',
			date : 93,
			mime_type : 'aioEkIJ9lmqur0C6',
			size : -8026335694059196693,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'BXy6RtEzi2wDks0T',
				),
				$client->photoSize(
					type : 'nlphPJTDY9somu0C',
					w : 88,
					h : 66,
					size : 50,
				),
				$client->photoCachedSize(
					type : 'tcsS1iWA8XRxOnpT',
					w : 44,
					h : 13,
					bytes : '??p?LiveProto? y??',
				),
				$client->photoStrippedSize(
					type : 'FhuWDbCEk8i0zYL7',
					bytes : '~?$}?LiveProtou2(??',
				),
				$client->photoSizeProgressive(
					type : 'npT8QokwH5yY2isV',
					w : 68,
					h : 90,
					sizes : array(57),
				),
				$client->photoPathSize(
					type : 'M5FWKH21aAjs97ZD',
					bytes : 'U^$LiveProto?Y?^e',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'NPmvbugSKfJqo1kM',
					w : 93,
					h : 77,
					size : 90,
					video_start_ts : -1395990.732421875,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : -137405630001184732,
					background_colors : array(52),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 10234002928102057,
					background_colors : array(53),
				),
			),
			dc_id : 15,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 61,
					h : 86,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'jXQHi29gr67vtBxC',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -1506234.9794921875,
					w : 50,
					h : 100,
					preload_prefix_size : 87,
					video_start_ts : 2006207.607421875,
					video_codec : 'Rcsg0boJfNmKS8wz',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 5,
					title : 'HwjgcpG76fXtINv4',
					performer : 'jATXMBiOVQtGDb3c',
					waveform : '?,
]LiveProto?6T',
				),
				$client->documentAttributeFilename(
					file_name : 'RiuNe8fKwbq1oGrE',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'LNQOAYKMGvkJpZPi',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```