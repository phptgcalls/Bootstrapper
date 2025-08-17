# inputBotInlineMessageMediaInvoice

**Description** : *An invoice*

**Layer** : 211

```tl
inputBotInlineMessageMediaInvoice#d7e78225 flags:# title:string description:string photo:flags.0?InputWebDocument invoice:Invoice payload:bytes provider:string provider_data:DataJSON reply_markup:flags.2?ReplyMarkup = InputBotInlineMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>title</mark> | [`string`](type/string) | Product name, 1-32 characters |
| <mark>description</mark> | [`string`](type/string) | Product description, 1-255 characters |
| **photo** | [`flags.0?InputWebDocument`](type/InputWebDocument) | Invoice photo |
| <mark>invoice</mark> | [`Invoice`](type/Invoice) | The invoice |
| <mark>payload</mark> | [`bytes`](type/bytes) | Bot-defined invoice payload, 1-128 bytes. This will not be displayed to the user, use for your internal processes |
| <mark>provider</mark> | [`string`](type/string) | Payments provider token, obtained via Botfather |
| <mark>provider_data</mark> | [`DataJSON`](type/DataJSON) | A JSON-serialized object for data about the invoice, which will be shared with the payment provider. A detailed description of the required fields should be provided by the payment provider |
| **reply_markup** | [`flags.2?ReplyMarkup`](type/ReplyMarkup) | Inline keyboard |

---

## Type

[InputBotInlineMessage](type/InputBotInlineMessage)

---

## Example

```php
$inputBotInlineMessage = $client->inputBotInlineMessageMediaInvoice(
	title : 'caXHJtMdg7LIzV0Q',
	description : 'uSIDGPrjAQHf6Fi9',
	photo : $client->inputWebDocument(
		url : 'https://docs.liveproto.dev',
		size : 20,
		mime_type : 'kaF1Ng3BW0vSGxQs',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 66,
				h : 1,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'Kvh20xqugnHRwQrL',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : -601946.5546875,
				w : 28,
				h : 17,
				preload_prefix_size : 61,
				video_start_ts : 305407.134765625,
				video_codec : 'JMgvxkAFuqch63y5',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 89,
				title : '5mKSfY3qF6LzctEk',
				performer : 'CFzRKLEGYHTtIsdX',
				waveform : 'M>?]LiveProto<4U/?',
			),
			$client->documentAttributeFilename(
				file_name : 'BrFylQtm8sHCwZ5A',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'QPepvDTlsxLFRUJb',
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
		currency : 'ZQNiAHVOEqUjzIbW',
		prices : array(
			$client->labeledPrice(
				label : 'b47lOmgASLfkRxqh',
				amount : 5968545748669410339,
			),
		),
		max_tip_amount : 1627849729971772280,
		suggested_tip_amounts : array(-195628974728470026),
		terms_url : 'https://docs.liveproto.dev',
		subscription_period : 31,
	),
	payload : '?{,-LiveProto??\\?',
	provider : 'wHx72BAC3rb4IPSM',
	provider_data : $client->dataJSON(
		data : 'QowXvpKGrS08mCTN',
	),
	reply_markup : $client->replyKeyboardHide(
		selective : true,
	),
);
```