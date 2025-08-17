# webPageAttributeTheme

**Description** : *Page theme*

**Layer** : 211

```tl
webPageAttributeTheme#54b56617 flags:# documents:flags.0?Vector<Document> settings:flags.1?ThemeSettings = WebPageAttribute;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **documents** | [`flags.0?Vector<Document>`](type/Document) | Theme files |
| **settings** | [`flags.1?ThemeSettings`](type/ThemeSettings) | Theme settings |

---

## Type

[WebPageAttribute](type/WebPageAttribute)

---

## Example

```php
$webPageAttribute = $client->webPageAttributeTheme(
	documents : array(
		$client->documentEmpty(
			id : -492860728643121411,
		),
		$client->document(
			id : -1680717731665532388,
			access_hash : -3032508801169831530,
			file_reference : 'hס?LiveProto??2?o',
			date : 97,
			mime_type : 'tSkMnbmVov5ZXNyf',
			size : -2607434957542811123,
			thumbs : array(
				$client->photoSizeEmpty(
					type : 'IUugwFE9WMkbcsC8',
				),
				$client->photoSize(
					type : '1Rdg9W3iBPXGJsEq',
					w : 46,
					h : 65,
					size : 45,
				),
				$client->photoCachedSize(
					type : 'pn9rIBvkwbSGc3Ql',
					w : 86,
					h : 59,
					bytes : '?B^ݮLiveProto	??>/',
				),
				$client->photoStrippedSize(
					type : '3KFm1zlHT9VeXCwg',
					bytes : '?B6?LiveProto????',
				),
				$client->photoSizeProgressive(
					type : 'QyLbWxG7iKcjSUDk',
					w : 4,
					h : 73,
					sizes : array(25),
				),
				$client->photoPathSize(
					type : 'onUGKewSxM9drzkN',
					bytes : ',̲?LiveProtoe?uw',
				),
			),
			video_thumbs : array(
				$client->videoSize(
					type : 'VjbHuyq5PTcd9A2Z',
					w : 56,
					h : 70,
					size : 3,
					video_start_ts : -217503.4169921875,
				),
				$client->videoSizeEmojiMarkup(
					emoji_id : -4133217685355841458,
					background_colors : array(78),
				),
				$client->videoSizeStickerMarkup(
					stickerset : $client->inputStickerSetEmpty(...),
					sticker_id : 6920001923889223674,
					background_colors : array(28),
				),
			),
			dc_id : 14,
			attributes : array(
				$client->documentAttributeImageSize(
					w : 15,
					h : 98,
				),
				$client->documentAttributeAnimated(),
				$client->documentAttributeSticker(
					mask : true,
					alt : 'pWYNzEjMtrGZbL1X',
					stickerset : $client->inputStickerSetEmpty(...),
					mask_coords : $client->maskCoords(...),
				),
				$client->documentAttributeVideo(
					round_message : true,
					supports_streaming : true,
					nosound : true,
					duration : 1868475.564453125,
					w : 54,
					h : 75,
					preload_prefix_size : 47,
					video_start_ts : -1402908.5283203125,
					video_codec : 'fRWdbvYOx8PeBGjJ',
				),
				$client->documentAttributeAudio(
					voice : true,
					duration : 41,
					title : 'Dxt1MEbX2c8T6YKH',
					performer : 'pP8TAwGEm5oJISB3',
					waveform : '????GLiveProtog?}f',
				),
				$client->documentAttributeFilename(
					file_name : 'Umhzf7ow5DybiuxQ',
				),
				$client->documentAttributeHasStickers(),
				$client->documentAttributeCustomEmoji(
					free : true,
					text_color : true,
					alt : 'W0QzgbT2DFedGvkA',
					stickerset : $client->inputStickerSetEmpty(...),
				),
			),
		),
	),
	settings : $client->themeSettings(
		message_colors_animated : true,
		base_theme : $client->baseThemeClassic(),
		accent_color : 57,
		outbox_accent_color : 10,
		message_colors : array(5),
		wallpaper : $client->wallPaper(
			id : 9168979348963581676,
			creator : true,
			default : true,
			pattern : true,
			dark : true,
			access_hash : -6514925675255984870,
			slug : 'Wf3kmOU26lYuXxpo',
			document : $client->documentEmpty(...),
			settings : $client->wallPaperSettings(...),
		),
	),
);
```