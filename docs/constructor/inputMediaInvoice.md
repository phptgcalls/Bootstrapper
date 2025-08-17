# inputMediaInvoice

**Description** : *Generated invoice of a bot payment*

**Layer** : 211

```tl
inputMediaInvoice#405fef0d flags:# title:string description:string photo:flags.0?InputWebDocument invoice:Invoice payload:bytes provider:flags.3?string provider_data:DataJSON start_param:flags.1?string extended_media:flags.2?InputMedia = InputMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>title</mark> | [`string`](type/string) | Product name, 1-32 characters |
| <mark>description</mark> | [`string`](type/string) | Product description, 1-255 characters |
| **photo** | [`flags.0?InputWebDocument`](type/InputWebDocument) | URL of the product photo for the invoice. Can be a photo of the goods or a marketing image for a service. People like it better when they see what they are paying for |
| <mark>invoice</mark> | [`Invoice`](type/Invoice) | The actual invoice |
| <mark>payload</mark> | [`bytes`](type/bytes) | Bot-defined invoice payload, 1-128 bytes. This will not be displayed to the user, use for your internal processes |
| **provider** | [`flags.3?string`](type/string) | Payments provider token, obtained via Botfather |
| <mark>provider_data</mark> | [`DataJSON`](type/DataJSON) | JSON-encoded data about the invoice, which will be shared with the payment provider. A detailed description of required fields should be provided by the payment provider |
| **start_param** | [`flags.1?string`](type/string) | Unique bot deep links start parameter. If present, forwarded copies of the sent message will have a URL button with a deep link to the bot (instead of a Pay button), with the value used as the start parameter. If absent, forwarded copies of the sent message will have a Pay button, allowing multiple users to pay directly from the forwarded message, using the same invoice |
| **extended_media** | [`flags.2?InputMedia`](type/InputMedia) | Deprecated |

---

## Type

[InputMedia](type/InputMedia)

---

## Example

```php
$inputMedia = $client->inputMediaInvoice(
	title : 'L7sa0qP2oKmvMQur',
	description : 'k2mGXyuVRpIOzjgN',
	photo : $client->inputWebDocument(
		url : 'https://docs.liveproto.dev',
		size : 10,
		mime_type : 'mytW3wY9ekn2sAMb',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 66,
				h : 25,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'yOd2EwM8jscLAavP',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : 1586794.5693359375,
				w : 4,
				h : 77,
				preload_prefix_size : 41,
				video_start_ts : 1009324.9638671875,
				video_codec : 'kXpeI2cMGBSvYjrE',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 68,
				title : 'UwhcKpZPRiTfSgOM',
				performer : 'hZNAayCPsvWDSGc4',
				waveform : '???O?LiveProtou???;',
			),
			$client->documentAttributeFilename(
				file_name : 'SQ94fbBkGeAZqNvm',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'f9GspytOhkYA2DbM',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	invoice : $client->invoice(
		test : true,
		name_requested : true,
		phone_requested : true,
		email_requested : true,
		shipping_address_requested : true,
		flexible : true,
		phone_to_provider : true,
		email_to_provider : true,
		recurring : true,
		currency : 'cs1y4NJjiARqra2C',
		prices : array(
			$client->labeledPrice(
				label : 'RtdMuTnrm6XHLvFY',
				amount : -7562044420641082537,
			),
		),
		max_tip_amount : 433740732746870875,
		suggested_tip_amounts : array(-2537050095500290524),
		terms_url : 'https://docs.liveproto.dev',
		subscription_period : 23,
	),
	payload : 'Uh???LiveProto	m???',
	provider : '9B60z8JKcmiFohQP',
	provider_data : $client->dataJSON(
		data : 'XvbKmrA9O6JiTgGc',
	),
	start_param : 'pJwibL7GHAg5q4ld',
	extended_media : $client->inputMediaEmpty(),
);
```