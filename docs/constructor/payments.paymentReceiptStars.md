# payments.paymentReceiptStars

**Description** : *Receipt for payment made using Telegram Stars*

**Layer** : 211

```tl
payments.paymentReceiptStars#dabbf83a flags:# date:int bot_id:long title:string description:string photo:flags.2?WebDocument invoice:Invoice currency:string total_amount:long transaction_id:string users:Vector<User> = payments.PaymentReceipt;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>date</mark> | [`int`](type/int) | Date of generation |
| <mark>bot_id</mark> | [`long`](type/long) | Bot ID |
| <mark>title</mark> | [`string`](type/string) | Title |
| <mark>description</mark> | [`string`](type/string) | Description |
| **photo** | [`flags.2?WebDocument`](type/WebDocument) | Product photo |
| <mark>invoice</mark> | [`Invoice`](type/Invoice) | Invoice |
| <mark>currency</mark> | [`string`](type/string) | Currency, always XTR |
| <mark>total_amount</mark> | [`long`](type/long) | Amount of Telegram Stars |
| <mark>transaction_id</mark> | [`string`](type/string) | Transaction ID |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about users mentioned in the other fields |

---

## Type

[payments.PaymentReceipt](type/payments.PaymentReceipt)

---

## Example

```php
$paymentsPaymentReceipt = $client->payments->paymentReceiptStars(
	date : 20,
	bot_id : -6440033326402762147,
	title : 'm4A3y5FzuHJSjNGM',
	description : '40f65XMs1ElVRo8c',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -8237827984284717321,
		size : 57,
		mime_type : 'uRSH4pTlWeEFAJzC',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 5,
				h : 46,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'i9MqwHj4lbdtGy6S',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : 446040.779296875,
				w : 15,
				h : 21,
				preload_prefix_size : 74,
				video_start_ts : -1257470.1318359375,
				video_codec : '6j5TaxM8GP7YeCHy',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 95,
				title : 'fILPF0kNcld5irmw',
				performer : 'g8NW16ITvD2q7BMk',
				waveform : '??*[]LiveProtoUP?x?',
			),
			$client->documentAttributeFilename(
				file_name : 'Xu0ht5VezvmT6P7w',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'FJwILR4fh3tH9BEX',
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
		currency : 'pYlkIh12ruzcVjS4',
		prices : array(
			$client->labeledPrice(
				label : 'ZdcELWvDgfSykM2s',
				amount : 8208354275770057072,
			),
		),
		max_tip_amount : -5349598306634230939,
		suggested_tip_amounts : array(-161901150458217106),
		terms_url : 'https://docs.liveproto.dev',
		subscription_period : 39,
	),
	currency : 'Fn68cCa3ZzHp1kmG',
	total_amount : 3368709191337393169,
	transaction_id : 'GsmPM1jfk5QoI0hv',
	users : array(
		$client->userEmpty(
			id : 2373605336263163126,
		),
		$client->user(
			self : true,
			contact : true,
			mutual_contact : true,
			deleted : true,
			bot : true,
			bot_chat_history : true,
			bot_nochats : true,
			verified : true,
			restricted : true,
			min : true,
			bot_inline_geo : true,
			support : true,
			scam : true,
			apply_min_photo : true,
			fake : true,
			bot_attach_menu : true,
			premium : true,
			attach_menu_enabled : true,
			bot_can_edit : true,
			close_friend : true,
			stories_hidden : true,
			stories_unavailable : true,
			contact_require_premium : true,
			bot_business : true,
			bot_has_main_app : true,
			id : -7628148346678173144,
			access_hash : -2950628650797854925,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 37,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'tsVnjDMpeTdSzLfP',
					reason : '9RVyXcUOvWkPMSAh',
					text : 'Ri9xHvoZBga4jTcy',
				),
			),
			bot_inline_placeholder : 'cIhRJPKtgB8DVp7s',
			lang_code : 'G3chQxnCg6moy4pF',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 25,
			color : $client->peerColor(
				color : 7,
				background_emoji_id : 1114215225888531990,
			),
			profile_color : $client->peerColor(
				color : 13,
				background_emoji_id : 6225455363105233417,
			),
			bot_active_users : 64,
			bot_verification_icon : 5882567801570734495,
			send_paid_messages_stars : -924300487835540257,
		),
	),
);
```