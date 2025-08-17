# botInlineMessageMediaInvoice

**Description** : *Send an invoice*

**Layer** : 211

```tl
botInlineMessageMediaInvoice#354a9b09 flags:# shipping_address_requested:flags.1?true test:flags.3?true title:string description:string photo:flags.0?WebDocument currency:string total_amount:long reply_markup:flags.2?ReplyMarkup = BotInlineMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **shipping_address_requested** | [`flags.1?true`](type/true) | Set this flag if you require the user's shipping address to complete the order |
| **test** | [`flags.3?true`](type/true) | Test invoice |
| <mark>title</mark> | [`string`](type/string) | Product name, 1-32 characters |
| <mark>description</mark> | [`string`](type/string) | Product description, 1-255 characters |
| **photo** | [`flags.0?WebDocument`](type/WebDocument) | Product photo |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code, or XTR for Telegram Stars |
| <mark>total_amount</mark> | [`long`](type/long) | Total price in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Inline keyboard |

---

## Type

[BotInlineMessage](type/BotInlineMessage)

---

## Example

```php
$botInlineMessage = $client->botInlineMessageMediaInvoice(
	shipping_address_requested : true,
	test : true,
	title : 'cUoefCdw5pTASRJ8',
	description : 'MamPyGtXYDzEA6rK',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -3217319671228815064,
		size : 81,
		mime_type : 'FQzbUs4u7e8tAXOZ',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 90,
				h : 41,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'tbSoF8ckRA4aON93',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : -2019239.55078125,
				w : 19,
				h : 20,
				preload_prefix_size : 88,
				video_start_ts : -1572843.9150390625,
				video_codec : 'wQa0pvlyfDOxB1Ht',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 0,
				title : 'Xa3fn164PsCRFtTj',
				performer : '7ALOid4Z5VlBmzWk',
				waveform : '??eLiveProto?4j\'
',
			),
			$client->documentAttributeFilename(
				file_name : '5uazKU3LvdEMc7W2',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'FyEgj1skMTpevZAC',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	currency : 'd7k0zHGBAfNM9wph',
	total_amount : -1607236474617495302,
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```