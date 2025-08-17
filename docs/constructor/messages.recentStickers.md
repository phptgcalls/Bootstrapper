# messages.recentStickers

**Description** : *Recently used stickers*

**Layer** : 211

```tl
messages.recentStickers#88d37c56 hash:long packs:Vector<StickerPack> stickers:Vector<Document> dates:Vector<int> = messages.RecentStickers;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`long`](type/long) | Hash used for caching, for more info click here |
| <mark>packs</mark> | [`Vector<StickerPack>`](type/StickerPack) | Emojis associated to stickers |
| <mark>stickers</mark> | [`Vector<Document>`](type/Document) | Recent stickers |
| <mark>dates</mark> | [`Vector<int>`](type/int) | When was each sticker last used |

---

## Type

[messages.RecentStickers](type/messages.RecentStickers)

---

## Example

```php
$messagesRecentStickers = $client->messages->recentStickers(
	hash : -5869340933411944767,
	packs : array(
		$client->stickerPack(
			emoticon : 'mM6PnGXiEt8xTqFs',
			documents : array(6412715845088329567),
		),
	),
	stickers : array(
		$client->documentEmpty(
			id : -4116654131390802590,
		),
		$client->document(
			id : -3360944048722699951,
			access_hash : 9018321818100499046,
			file_reference : 'X???hLiveProto[???q',
			date : 26,
			mime_type : '6DSlefCv1aKFcd57',
			size : -2244091476074490894,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'VJTGWZ354mpav0Lq',
				),
				$client->photoSize(
					type : 'Set1bQo87fRhJNPv',
					w : 42,
					h : 41,
					size : 4,
				),
				$client->photoCachedSize(
					type : 'YWocJgpBjXvlqxbZ',
					w : 97,
					h : 98,
					bytes : 'N0k?LiveProtoK2?.}',
				),
				$client->photoStrippedSize(
					type : 'SZDLimROnPou9KvM',
					bytes : '???-LiveProto)??',
				),
				$client->photoSizeProgressive(
					type : '70vh5ndqOzLlp2wy',
					w : 78,
					h : 40,
					sizes : array(46),
				),
				$client->photoPathSize(
					type : 'CqclrKGWOa5wVyPv',
					bytes : '`ZT?9LiveProtoӯ???',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : '3Kx94BIbQ8oYUX1a',
					w : 49,
					h : 16,
					size : 32,
					video_start_ts : 1412375.4658203125,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 4773915092462084606,
					background_colors : array(98),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 7655850030597152378,
					background_colors : array(33),
				),
			),
			dc_id : 10,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 84,
					h : 49,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'wsNapnd9TBYGv2cR',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : -1011611.521484375,
					w : 57,
					h : 8,
					preload_prefix_size : 50,
					video_start_ts : 520504.1796875,
					video_codec : 'mI6XyQkgJxANp5oM',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 92,
					title : 'ErgnMFD8CoIscbGA',
					performer : '6F5DXhGYHVMUbmES',
					waveform : 'b?ܞ?LiveProto??
;?',
				),
				$client->documentAttributeFilename(
					file_name : 'TRu8teoJl9Iqfyvi',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'DxfOXRqrJYo216ym',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
	dates : array(69),
);
```