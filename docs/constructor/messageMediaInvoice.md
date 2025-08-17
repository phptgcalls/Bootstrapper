# messageMediaInvoice

**Description** : *Invoice*

**Layer** : 211

```tl
messageMediaInvoice#f6a548d3 flags:# shipping_address_requested:flags.1?true test:flags.3?true title:string description:string photo:flags.0?WebDocument receipt_msg_id:flags.2?int currency:string total_amount:long start_param:string extended_media:flags.4?MessageExtendedMedia = MessageMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **shipping_address_requested** | [`flags.1?true`](type/true) | Whether the shipping address was requested |
| **test** | [`flags.3?true`](type/true) | Whether this is an example invoice |
| <mark>title</mark> | [`string`](type/string) | Product name, 1-32 characters |
| <mark>description</mark> | [`string`](type/string) | Product description, 1-255 characters |
| **photo** | [`flags.0?WebDocument`](type/WebDocument) | URL of the product photo for the invoice. Can be a photo of the goods or a marketing image for a service. People like it better when they see what they are paying for |
| **receipt_msg_id** | [`flags.2?int`](type/int) | Message ID of receipt: if set, clients should change the text of the first keyboardButtonBuy button always attached to the message to a localized version of the word Receipt |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code, or XTR for Telegram Stars |
| <mark>total_amount</mark> | [`long`](type/long) | Total price in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |
| <mark>start_param</mark> | [`string`](type/string) | Unique bot deep-linking parameter that can be used to generate this invoice |
| **extended_media** | [`flags.4?MessageExtendedMedia`](type/MessageExtendedMedia) | Deprecated |

---

## Type

[MessageMedia](type/MessageMedia)

---

## Example

```php
$messageMedia = $client->messageMediaInvoice(
	shipping_address_requested : true,
	test : true,
	title : 'ZKfq89zmnvSIHayB',
	description : '2HZkm7WNI8vXJCSb',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -4970552874899795442,
		size : 92,
		mime_type : 'Qbzsu7eRtvSLnWdh',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 92,
				h : 9,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'SYgnVk3XpGE17RmK',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : 2083695.4248046875,
				w : 22,
				h : 81,
				preload_prefix_size : 50,
				video_start_ts : 1840112.83203125,
				video_codec : '8kovuHtB0mJai73Z',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 8,
				title : 'hN9bV1X7lj3ZSzDy',
				performer : '8hLnMTtDcebm3EZQ',
				waveform : 'k3??LiveProtoƖW؁',
			),
			$client->documentAttributeFilename(
				file_name : 'GWTwiXSYzsb3JtcN',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'tOVw5q4Xmv1QycNn',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	receipt_msg_id : 84,
	currency : '04gEosBCV7NyAl2n',
	total_amount : 3503046249894960922,
	start_param : 'WDeshx4FmP5XiAEt',
	extended_media : $client->messageExtendedMediaPreview(
		w : 9,
		h : 57,
		thumb : $client->photoSizeEmpty(
			type : 'bhW9FXSePf2NCI6m',
		),
		video_duration : 10,
	),
);
```