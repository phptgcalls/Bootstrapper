# inputBotInlineResult

**Description** : *An inline bot result*

**Layer** : 211

```tl
inputBotInlineResult#88bf9319 flags:# id:string type:string title:flags.1?string description:flags.2?string url:flags.3?string thumb:flags.4?InputWebDocument content:flags.5?InputWebDocument send_message:InputBotInlineMessage = InputBotInlineResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>id</mark> | [`string`](type/string) | ID of result |
| <mark>type</mark> | [`string`](type/string) | Result type (see bot API docs) |
| **title** | [`flags.1?string`](type/string) | Result title |
| **description** | [`flags.2?string`](type/string) | Result description |
| **url** | [`flags.3?string`](type/string) | URL of result |
| **thumb** | [`flags.4?InputWebDocument`](type/InputWebDocument) | Thumbnail for result |
| **content** | [`flags.5?InputWebDocument`](type/InputWebDocument) | Result contents |
| <mark>send_message</mark> | [`InputBotInlineMessage`](type/InputBotInlineMessage) | Message to send when the result is selected |

---

## Type

[InputBotInlineResult](type/InputBotInlineResult)

---

## Example

```php
$inputBotInlineResult = $client->inputBotInlineResult(
	id : 'ovC7bEN394XDJsUf',
	type : 'KxYoHsnuNLrTWvZ7',
	title : 'pZw7ieCTYv1BRPIm',
	description : 'd0iKO3spVAHghJex',
	url : 'https://docs.liveproto.dev',
	thumb : $client->inputWebDocument(
		url : 'https://docs.liveproto.dev',
		size : 95,
		mime_type : 'SOq835MYtTp6dAmH',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 56,
				h : 77,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'L4jJomTyrhvt3GOC',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : 1446042.779296875,
				w : 55,
				h : 88,
				preload_prefix_size : 93,
				video_start_ts : -2087082.248046875,
				video_codec : 'wXCoPaViGqp1juDk',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 89,
				title : 'jiOhbvPVtEyW0Mgd',
				performer : 'kdB85UFyYRT2eHpi',
				waveform : '{eZLiveProto?n2?',
			),
			$client->documentAttributeFilename(
				file_name : 'P9KWgEYsqRo8x2Uc',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'C1QI8JuhL2V0ZKFX',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	content : $client->inputWebDocument(
		url : 'https://docs.liveproto.dev',
		size : 98,
		mime_type : 'p0Cbs6UoRdj7G1f3',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 94,
				h : 32,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : '4YVEpKtdqDyMjwUZ',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : -784891.71875,
				w : 59,
				h : 36,
				preload_prefix_size : 63,
				video_start_ts : -2084608.8046875,
				video_codec : '8mYNhgrA0O1vojBQ',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 23,
				title : 'GZtvi0UylpL2YTQK',
				performer : 'mpUhXKABoLskziOT',
				waveform : '*5?6LiveProto,??',
			),
			$client->documentAttributeFilename(
				file_name : 'Nqxk3fTi2gy6GAHv',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'os0lSQA1rcuLCa6v',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	send_message : $client->inputBotInlineMessageMediaAuto(
		invert_media : true,
		message : 'AclYuap97gNnH4Oj',
		entities : array(
			$client->messageEntityUnknown(
				offset : 77,
				length : 94,
			),
			$client->messageEntityMention(
				offset : 19,
				length : 85,
			),
			$client->messageEntityHashtag(
				offset : 74,
				length : 28,
			),
			$client->messageEntityBotCommand(
				offset : 63,
				length : 25,
			),
			$client->messageEntityUrl(
				offset : 88,
				length : 92,
			),
			$client->messageEntityEmail(
				offset : 58,
				length : 87,
			),
			$client->messageEntityBold(
				offset : 14,
				length : 91,
			),
			$client->messageEntityItalic(
				offset : 11,
				length : 83,
			),
			$client->messageEntityCode(
				offset : 16,
				length : 92,
			),
			$client->messageEntityPre(
				offset : 59,
				length : 57,
				language : 'h21JL5pco9HAPZdC',
			),
			$client->messageEntityTextUrl(
				offset : 11,
				length : 70,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 63,
				length : 32,
				user_id : -7115795093442637636,
			),
			$client->inputMessageEntityMentionName(
				offset : 98,
				length : 55,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 16,
				length : 92,
			),
			$client->messageEntityCashtag(
				offset : 39,
				length : 28,
			),
			$client->messageEntityUnderline(
				offset : 52,
				length : 1,
			),
			$client->messageEntityStrike(
				offset : 77,
				length : 52,
			),
			$client->messageEntityBankCard(
				offset : 88,
				length : 16,
			),
			$client->messageEntitySpoiler(
				offset : 22,
				length : 22,
			),
			$client->messageEntityCustomEmoji(
				offset : 8,
				length : 84,
				document_id : -1897959127069768070,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 87,
				length : 85,
			),
		),
		reply_markup : $client->replyKeyboardHide(
			selective : true,
		),
	),
);
```