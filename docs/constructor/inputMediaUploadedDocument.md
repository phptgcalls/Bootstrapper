# inputMediaUploadedDocument

**Description** : *New document*

**Layer** : 211

```tl
inputMediaUploadedDocument#37c9330 flags:# nosound_video:flags.3?true force_file:flags.4?true spoiler:flags.5?true file:InputFile thumb:flags.2?InputFile mime_type:string attributes:Vector<DocumentAttribute> stickers:flags.0?Vector<InputDocument> video_cover:flags.6?InputPhoto video_timestamp:flags.7?int ttl_seconds:flags.1?int = InputMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **nosound_video** | [`flags.3?true`](type/true) | Whether the specified document is a video file with no audio tracks (a GIF animation (even as MPEG4), for example) |
| **force_file** | [`flags.4?true`](type/true) | Force the media file to be uploaded as document |
| **spoiler** | [`flags.5?true`](type/true) | Whether this media should be hidden behind a spoiler warning |
| <mark>file</mark> | [`InputFile`](type/InputFile) | The uploaded file |
| **thumb** | [`flags.2?InputFile`](type/InputFile) | Thumbnail of the document, uploaded as for the file |
| <mark>mime_type</mark> | [`string`](type/string) | MIME type of document |
| <mark>attributes</mark> | [`Vector<DocumentAttribute>`](type/DocumentAttribute) | Attributes that specify the type of the document (video, audio, voice, sticker, etc.) |
| **stickers** | [`flags.0?Vector<InputDocument>`](type/InputDocument) | Attached stickers |
| **video_cover** | [`flags.6?InputPhoto`](type/InputPhoto) | NOTHING |
| **video_timestamp** | [`flags.7?int`](type/int) | NOTHING |
| **ttl_seconds** | [`flags.1?int`](type/int) | Time to live in seconds of self-destructing document |

---

## Type

[InputMedia](type/InputMedia)

---

## Example

```php
$inputMedia = $client->inputMediaUploadedDocument(
	nosound_video : true,
	force_file : true,
	spoiler : true,
	file : $client->inputFile(
		id : -6203384783310537155,
		parts : 74,
		name : '1LoiI6lwxuQOSY5G',
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
	),
	thumb : $client->inputFile(
		id : -8430445668605687769,
		parts : 23,
		name : 'TewmaN1pBLyHOvX0',
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
	),
	mime_type : 'sDJlfPwY7HSRt1Qi',
	attributes : array(
		$client->documentAttributeImageSize(
			w : 54,
			h : 4,
		),
		$client->documentAttributeAnimated(),
		$client->documentAttributeSticker(
			mask : true,
			alt : 'xeTJyPt4lISBU8Rp',
			stickerset : $client->inputStickerSetEmpty(),
			mask_coords : $client->maskCoords(
				n : 61,
				x : -1501830.619140625,
				y : -293031.7763671875,
				zoom : 1942235.787109375,
			),
		),
		$client->documentAttributeVideo(
			round_message : true,
			supports_streaming : true,
			nosound : true,
			duration : 314119.4853515625,
			w : 39,
			h : 21,
			preload_prefix_size : 12,
			video_start_ts : 159671.8193359375,
			video_codec : '7pOUI6aQCk05MZA9',
		),
		$client->documentAttributeAudio(
			voice : true,
			duration : 67,
			title : '3QoARm6dShrVOLai',
			performer : 'DEbcgQMnhVPqKOaI',
			waveform : 'y??<?LiveProto^ ??',
		),
		$client->documentAttributeFilename(
			file_name : 'Hyj58gsKiBAQ6xkt',
		),
		$client->documentAttributeHasStickers(),
		$client->documentAttributeCustomEmoji(
			free : true,
			text_color : true,
			alt : '97j1biGhBmksw5lz',
			stickerset : $client->inputStickerSetEmpty(),
		),
	),
	stickers : array(
		$client->inputDocumentEmpty(),
		$client->inputDocument(
			id : 6860217150061672841,
			access_hash : -1785974418513124516,
			file_reference : '?"&?LiveProto??nZZ',
		),
	),
	video_cover : $client->inputPhotoEmpty(),
	video_timestamp : 37,
	ttl_seconds : 56,
);
```