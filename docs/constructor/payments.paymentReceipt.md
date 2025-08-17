# payments.paymentReceipt

**Description** : *Receipt*

**Layer** : 211

```tl
payments.paymentReceipt#70c4fe03 flags:# date:int bot_id:long provider_id:long title:string description:string photo:flags.2?WebDocument invoice:Invoice info:flags.0?PaymentRequestedInfo shipping:flags.1?ShippingOption tip_amount:flags.3?long currency:string total_amount:long credentials_title:string users:Vector<User> = payments.PaymentReceipt;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>date</mark> | [`int`](type/int) | Date of generation |
| <mark>bot_id</mark> | [`long`](type/long) | Bot ID |
| <mark>provider_id</mark> | [`long`](type/long) | Provider ID |
| <mark>title</mark> | [`string`](type/string) | Title |
| <mark>description</mark> | [`string`](type/string) | Description |
| **photo** | [`flags.2?WebDocument`](type/WebDocument) | Photo |
| <mark>invoice</mark> | [`Invoice`](type/Invoice) | Invoice |
| **info** | [`flags.0?PaymentRequestedInfo`](type/PaymentRequestedInfo) | Info |
| **shipping** | [`flags.1?ShippingOption`](type/ShippingOption) | Selected shipping option |
| **tip_amount** | [`flags.3?long`](type/long) | Tipped amount |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code |
| <mark>total_amount</mark> | [`long`](type/long) | Total amount in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |
| <mark>credentials_title</mark> | [`string`](type/string) | Payment credential name |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users |

---

## Type

[payments.PaymentReceipt](type/payments.PaymentReceipt)

---

## Example

```php
$paymentsPaymentReceipt = $client->payments->paymentReceipt(
	date : 9,
	bot_id : -6746166320818990802,
	provider_id : -1245607894168533413,
	title : '95S2yuc0Wo1vqIYM',
	description : 'uDLkz3IEidUasHV5',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -3267575686066448908,
		size : 41,
		mime_type : 'Gyw2YbL1Do5Ut3SF',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 14,
				h : 69,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'K4InOLDFjUtz2GoB',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : 1869310.7607421875,
				w : 33,
				h : 76,
				preload_prefix_size : 56,
				video_start_ts : 2086853.7939453125,
				video_codec : 'snwoadPM3cr61Y5p',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 39,
				title : 'okxCJzURSXNOvT50',
				performer : 'knHZ7FdBTN1JqhY9',
				waveform : ';?9?LiveProto8-???',
			),
			$client->documentAttributeFilename(
				file_name : 'BvgxJUDqCoskPeNG',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : '8m4sqEbANdurXzhT',
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
		currency : 'OHPjZBTiYRQJr1uS',
		prices : array(
			$client->labeledPrice(
				label : '5zeM0ybtOpSrXW32',
				amount : -7327837369387093502,
			),
		),
		max_tip_amount : 7053022469043068935,
		suggested_tip_amounts : array(5612938328270686371),
		terms_url : 'https://docs.liveproto.dev',
		subscription_period : 23,
	),
	info : $client->paymentRequestedInfo(
		name : 'pWGbJelg1s0SZVoK',
		phone : '+1234567890',
		email : 'reply@liveproto.dev',
		shipping_address : $client->postAddress(
			street_line1 : 'yoAH9cOS3rT7fL5q',
			street_line2 : 's4wMmKzJaUGx1peh',
			city : '2kXDJwGYQlZM1vAg',
			state : '67GOtfyXAsdgSTDn',
			country_iso2 : 'yASJzk4gr0KoIpZL',
			post_code : 'uYWgFNkiOrLlDKCZ',
		),
	),
	shipping : $client->shippingOption(
		id : 'oZ4XmG9SHQt3sLMA',
		title : 'Q5PGCTnM6ljZB9dm',
		prices : array(
			$client->labeledPrice(
				label : 'b9hiHralO1wnKj3f',
				amount : -3927234585187632734,
			),
		),
	),
	tip_amount : -317446098796462532,
	currency : 'hlLR0uCJYGrMmj6X',
	total_amount : 8597441700421838258,
	credentials_title : 'U5x6VKhnRSzYsbZl',
	users : array(
		$client->userEmpty(
			id : 3993688386366087341,
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
			id : 6922393474451724722,
			access_hash : 3356283965244633321,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 54,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '8LQREgpeCVfBmyjd',
					reason : 'PhLcFB4po3iwaUYe',
					text : 'yd4u5lWTGRCwQenz',
				),
			),
			bot_inline_placeholder : 'ycLA1fMqQd3BSY6X',
			lang_code : 'qhcT7aLSPCRyHvJW',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 72,
			color : $client->peerColor(
				color : 95,
				background_emoji_id : 7745767792354142353,
			),
			profile_color : $client->peerColor(
				color : 38,
				background_emoji_id : 3507903636917738832,
			),
			bot_active_users : 13,
			bot_verification_icon : -978710075770856342,
			send_paid_messages_stars : -6276155026191401593,
		),
	),
);
```