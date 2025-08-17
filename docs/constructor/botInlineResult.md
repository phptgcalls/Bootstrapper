# botInlineResult

**Description** : *Generic result*

**Layer** : 211

```tl
botInlineResult#11965f3a flags:# id:string type:string title:flags.1?string description:flags.2?string url:flags.3?string thumb:flags.4?WebDocument content:flags.5?WebDocument send_message:BotInlineMessage = BotInlineResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>id</mark> | [`string`](type/string) | Result ID |
| <mark>type</mark> | [`string`](type/string) | Result type (see bot API docs) |
| **title** | [`flags.1?string`](type/string) | Result title |
| **description** | [`flags.2?string`](type/string) | Result description |
| **url** | [`flags.3?string`](type/string) | URL of article or webpage |
| **thumb** | [`flags.4?WebDocument`](type/WebDocument) | Thumbnail for the result |
| **content** | [`flags.5?WebDocument`](type/WebDocument) | Content of the result |
| <mark>send_message</mark> | [`BotInlineMessage`](type/BotInlineMessage) | Message to send |

---

## Type

[BotInlineResult](type/BotInlineResult)

---

## Example

```php
$botInlineResult = $client->botInlineResult(
	id : 'Rh7TpWebnHtMJPmx',
	type : 'fZHwckTbDCBl517R',
	title : '5iPYq63jzBXNuUcp',
	description : 'ACaxKtw2ylEfIX5s',
	url : 'https://docs.liveproto.dev',
	thumb : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -5849165250119372493,
		size : 51,
		mime_type : 'XQHNGKmqTVaytRJ9',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 98,
				h : 68,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : '0nAXlP8vLOiWrUN4',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : -653023.140625,
				w : 37,
				h : 93,
				preload_prefix_size : 89,
				video_start_ts : -1397815.8896484375,
				video_codec : 'eGgNI7S1slwyChaY',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 60,
				title : 'lkBwivoy6nYK8U2x',
				performer : '1gi8z60uYPhmd9wE',
				waveform : '?39??LiveProto%?˿',
			),
			$client->documentAttributeFilename(
				file_name : 'Z2eS9QYmC0Akba4K',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'uFTpntfGHvqdrbQk',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	content : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : 7262916741561421373,
		size : 30,
		mime_type : 'aVJgy1NbzCw7QjKD',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 85,
				h : 16,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'qNiPyH9sCUchZIoK',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : -16059.3291015625,
				w : 55,
				h : 92,
				preload_prefix_size : 8,
				video_start_ts : 1652073.1962890625,
				video_codec : 'U9NnhaituxFSzO1E',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 16,
				title : 'nDI5LkzbZv0f72YA',
				performer : 'j8SuCIMoAcstaKf1',
				waveform : '??t?LiveProtoh??',
			),
			$client->documentAttributeFilename(
				file_name : 'iHpYth6TP2wFksSf',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'UewyKRSaPDm8QWuo',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	send_message : $client->botInlineMessageMediaAuto(
		invert_media : true,
		message : '4ZCn9jIhkAGEquHo',
		entities : array(
			$client->messageEntityUnknown(
				offset : 57,
				length : 91,
			),
			$client->messageEntityMention(
				offset : 95,
				length : 49,
			),
			$client->messageEntityHashtag(
				offset : 54,
				length : 18,
			),
			$client->messageEntityBotCommand(
				offset : 100,
				length : 51,
			),
			$client->messageEntityUrl(
				offset : 74,
				length : 57,
			),
			$client->messageEntityEmail(
				offset : 27,
				length : 44,
			),
			$client->messageEntityBold(
				offset : 7,
				length : 50,
			),
			$client->messageEntityItalic(
				offset : 6,
				length : 93,
			),
			$client->messageEntityCode(
				offset : 30,
				length : 91,
			),
			$client->messageEntityPre(
				offset : 88,
				length : 8,
				language : 'nhRBokGx7cpa85IZ',
			),
			$client->messageEntityTextUrl(
				offset : 8,
				length : 36,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 74,
				length : 50,
				user_id : 9185468191341101243,
			),
			$client->inputMessageEntityMentionName(
				offset : 21,
				length : 45,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 66,
				length : 5,
			),
			$client->messageEntityCashtag(
				offset : 38,
				length : 93,
			),
			$client->messageEntityUnderline(
				offset : 81,
				length : 45,
			),
			$client->messageEntityStrike(
				offset : 61,
				length : 83,
			),
			$client->messageEntityBankCard(
				offset : 52,
				length : 35,
			),
			$client->messageEntitySpoiler(
				offset : 29,
				length : 19,
			),
			$client->messageEntityCustomEmoji(
				offset : 60,
				length : 12,
				document_id : -6138538634744677310,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 50,
				length : 34,
			),
		),
		reply_markup : $client->replyKeyboardHide(
			selective : true,
		),
	),
);
```