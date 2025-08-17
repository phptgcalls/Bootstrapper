# payments.paymentFormStars

**Description** : *Represents a payment form, for payments to be using Telegram Stars, see here » for more info*

**Layer** : 211

```tl
payments.paymentFormStars#7bf6b15c flags:# form_id:long bot_id:long title:string description:string photo:flags.5?WebDocument invoice:Invoice users:Vector<User> = payments.PaymentForm;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>form_id</mark> | [`long`](type/long) | Form ID |
| <mark>bot_id</mark> | [`long`](type/long) | Bot ID |
| <mark>title</mark> | [`string`](type/string) | Form title |
| <mark>description</mark> | [`string`](type/string) | Description |
| **photo** | [`flags.5?WebDocument`](type/WebDocument) | Product photo |
| <mark>invoice</mark> | [`Invoice`](type/Invoice) | Invoice |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about users mentioned in the other fields |

---

## Type

[payments.PaymentForm](type/payments.PaymentForm)

---

## Example

```php
$paymentsPaymentForm = $client->payments->paymentFormStars(
	form_id : 5631681678377050873,
	bot_id : -3636125577847515654,
	title : 'j1IOCTfk3eadiFJs',
	description : 'SNqo6Mthd071s2DQ',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -1406512978396203791,
		size : 95,
		mime_type : 'pymxVigu56SUrEIc',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 49,
				h : 48,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'BL6HkbJngdY9cTND',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : 1050491.5029296875,
				w : 95,
				h : 0,
				preload_prefix_size : 55,
				video_start_ts : 1647051.875,
				video_codec : 'EIyinghC4jSKf8X3',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 97,
				title : 'eB1suYgFOvhX5QSZ',
				performer : 'GTp4jn5i0ERgCdeP',
				waveform : '?\'$?LiveProtoxVBk?',
			),
			$client->documentAttributeFilename(
				file_name : 'bVEhXMnBGUoYNZeD',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : 'r3dTkVi5gxqOQpwj',
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
		currency : '0sKgmj8ANl7wTp5i',
		prices : array(
			$client->labeledPrice(
				label : 'hrZxCNXVF5ygfv9a',
				amount : 1805733179163114491,
			),
		),
		max_tip_amount : 1572405684935692776,
		suggested_tip_amounts : array(-9108322829429716362),
		terms_url : 'https://docs.liveproto.dev',
		subscription_period : 79,
	),
	users : array(
		$client->userEmpty(
			id : 3727591914559913849,
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
			id : -1622648271379513888,
			access_hash : -7606269552940079359,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 4,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'oKTBeuEMGmblpcSQ',
					reason : 'vXjZFJA6fOYLeM0V',
					text : 'OPbTnSJLmGBWtkM0',
				),
			),
			bot_inline_placeholder : 'oKGiWRH5B3CTgQf9',
			lang_code : 'E8QxOCgF1SpJUVbm',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 57,
			color : $client->peerColor(
				color : 5,
				background_emoji_id : 8572055917706015277,
			),
			profile_color : $client->peerColor(
				color : 80,
				background_emoji_id : 3469021351263158830,
			),
			bot_active_users : 45,
			bot_verification_icon : 2978917137900445912,
			send_paid_messages_stars : -6466784140876006671,
		),
	),
);
```