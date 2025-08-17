# messages.availableEffects

**Description** : *The full list of usable animated message effects »*

**Layer** : 211

```tl
messages.availableEffects#bddb616e hash:int effects:Vector<AvailableEffect> documents:Vector<Document> = messages.AvailableEffects;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`int`](type/int) | Hash used for caching, for more info click here |
| <mark>effects</mark> | [`Vector<AvailableEffect>`](type/AvailableEffect) | Message effects |
| <mark>documents</mark> | [`Vector<Document>`](type/Document) | Documents specified in the effects constructors |

---

## Type

[messages.AvailableEffects](type/messages.AvailableEffects)

---

## Example

```php
$messagesAvailableEffects = $client->messages->availableEffects(
	hash : 29,
	effects : array(
		$client->availableEffect(
			premium_required : true,
			id : 2841126342964032779,
			emoticon : 'gNtCFfqb2GliQuaR',
			static_icon_id : -6001799566452127837,
			effect_sticker_id : 3771593368850406040,
			effect_animation_id : -8310238857797651191,
		),
	),
	documents : array(
		$client->documentEmpty(
			id : 8506739098200068510,
		),
		$client->document(
			id : -2368113492538628089,
			access_hash : -3608505516702584502,
			file_reference : '-c?MLiveProto?x??q',
			date : 7,
			mime_type : 'Le8KmUOWEP0GVd5A',
			size : 8591225015641003017,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'GQyWohPJus6Fb1j0',
				),
				$client->photoSize(
					type : 'jOJDGh189nl5BEwP',
					w : 18,
					h : 64,
					size : 33,
				),
				$client->photoCachedSize(
					type : 'xJ3kHpMoWUeq2hfy',
					w : 84,
					h : 34,
					bytes : '^?\'
?LiveProtoue??',
				),
				$client->photoStrippedSize(
					type : 'ReN6l2usbtjHvIFa',
					bytes : '?0??LiveProto-ۊ/?',
				),
				$client->photoSizeProgressive(
					type : '8ysjNc0vTBM2A7DS',
					w : 93,
					h : 99,
					sizes : array(54),
				),
				$client->photoPathSize(
					type : 'q905cjvxXyipO47Y',
					bytes : '??
$?LiveProto|y?h=',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'dqKv2fuO4aSQB0Ys',
					w : 96,
					h : 44,
					size : 61,
					video_start_ts : -1621996.4951171875,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : 295420258780120378,
					background_colors : array(28),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 5396352111956012604,
					background_colors : array(11),
				),
			),
			dc_id : 21,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 55,
					h : 56,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'r1tYh3uw0yqcSCgR',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 1117924.5126953125,
					w : 92,
					h : 38,
					preload_prefix_size : 22,
					video_start_ts : -1523987.099609375,
					video_codec : 'UyAw0h3NkMp19WBd',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 30,
					title : '9PodqjFfUBp2bwgr',
					performer : 'AJOLUN5rF2jGYBbi',
					waveform : 'm?ߞLiveProto?{??',
				),
				$client->documentAttributeFilename(
					file_name : 'Gp2LRk1wgBrdWzPj',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'yN8sdg6hqmxEiFOK',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
);
```