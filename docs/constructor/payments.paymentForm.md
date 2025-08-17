# payments.paymentForm

**Description** : *Payment form*

**Layer** : 211

```tl
payments.paymentForm#a0058751 flags:# can_save_credentials:flags.2?true password_missing:flags.3?true form_id:long bot_id:long title:string description:string photo:flags.5?WebDocument invoice:Invoice provider_id:long url:string native_provider:flags.4?string native_params:flags.4?DataJSON additional_methods:flags.6?Vector<PaymentFormMethod> saved_info:flags.0?PaymentRequestedInfo saved_credentials:flags.1?Vector<PaymentSavedCredentials> users:Vector<User> = payments.PaymentForm;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **can_save_credentials** | [`flags.2?true`](type/true) | Whether the user can choose to save credentials |
| **password_missing** | [`flags.3?true`](type/true) | Indicates that the user can save payment credentials, but only after setting up a 2FA password (currently the account doesn't have a 2FA password) |
| <mark>form_id</mark> | [`long`](type/long) | Form ID |
| <mark>bot_id</mark> | [`long`](type/long) | Bot ID |
| <mark>title</mark> | [`string`](type/string) | Form title |
| <mark>description</mark> | [`string`](type/string) | Description |
| **photo** | [`flags.5?WebDocument`](type/WebDocument) | Product photo |
| <mark>invoice</mark> | [`Invoice`](type/Invoice) | Invoice |
| <mark>provider_id</mark> | [`long`](type/long) | Payment provider ID |
| <mark>url</mark> | [`string`](type/string) | Payment form URL |
| **native_provider** | [`flags.4?string`](type/string) | Payment provider name.One of the following:- stripe |
| **native_params** | [`flags.4?DataJSON`](type/DataJSON) | Contains information about the payment provider, if available, to support it natively without the need for opening the URL.A JSON object that can contain the following fields:- apple_pay_merchant_id: Apple Pay merchant ID- google_pay_public_key: Google Pay public key- need_country: True, if the user country must be provided,- need_zip: True, if the user ZIP/postal code must be provided,- need_cardholder_name: True, if the cardholder name must be provided |
| **additional_methods** | [`flags.6?Vector<PaymentFormMethod>`](type/PaymentFormMethod) | Additional payment methods |
| **saved_info** | [`flags.0?PaymentRequestedInfo`](type/PaymentRequestedInfo) | Saved server-side order information |
| **saved_credentials** | [`flags.1?Vector<PaymentSavedCredentials>`](type/PaymentSavedCredentials) | Contains information about saved card credentials |
| <mark>users</mark> | [`Vector<User>`](type/User) | Users |

---

## Type

[payments.PaymentForm](type/payments.PaymentForm)

---

## Example

```php
$paymentsPaymentForm = $client->payments->paymentForm(
	can_save_credentials : true,
	password_missing : true,
	form_id : -7356916860711023533,
	bot_id : -4728449284769019922,
	title : 'nP4xiJW6ZpjzgGFl',
	description : 'Swy1x8vTmL0MlE4e',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -7181086718574273751,
		size : 36,
		mime_type : 'Hl7wuUIbizDFo2Wy',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 23,
				h : 25,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'do5MN3eUzVDrIg82',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : -399773.7353515625,
				w : 76,
				h : 80,
				preload_prefix_size : 38,
				video_start_ts : 1331221.37890625,
				video_codec : 'p2oIe9ZGCFVuzMW7',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 25,
				title : '4Z3pKt6iUc5GboPz',
				performer : '7gmVxONeQdJ4oYri',
				waveform : '??B?ULiveProto	??w',
			),
			$client->documentAttributeFilename(
				file_name : 'F8mMghC3n7iqGVHQ',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : '58fnQzImrSYw9Obx',
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
		currency : 'fk5aprnWw60Dx49B',
		prices : array(
			$client->labeledPrice(
				label : 'josTtmb7ulh5gOK8',
				amount : -505442384214270465,
			),
		),
		max_tip_amount : -4900486991795988385,
		suggested_tip_amounts : array(2680545580289539922),
		terms_url : 'https://docs.liveproto.dev',
		subscription_period : 4,
	),
	provider_id : 2912703834207351140,
	url : 'https://docs.liveproto.dev',
	native_provider : 'wimvJdT453XpOubG',
	native_params : $client->dataJSON(
		data : 'qTx1sfSHuk9pwoWE',
	),
	additional_methods : array(
		$client->paymentFormMethod(
			url : 'https://docs.liveproto.dev',
			title : '8HUic12l7rGqFR3Q',
		),
	),
	saved_info : $client->paymentRequestedInfo(
		name : 'aYmdHZeNDbgAxKjS',
		phone : '+1234567890',
		email : 'reply@liveproto.dev',
		shipping_address : $client->postAddress(
			street_line1 : 'nFKjqROEUdXYmetQ',
			street_line2 : 'uGWQyxTbt4o29gmN',
			city : '3eBCzvPoalNHQyEL',
			state : 'Slz5opTsPdnYqFe6',
			country_iso2 : '8vgEIrfNWV79wkG4',
			post_code : '4HTudpzr60Sfvjaw',
		),
	),
	saved_credentials : array(
		$client->paymentSavedCredentialsCard(
			id : 'I63v5w4qhBduQCEZ',
			title : 'txU6W8IrgN7XQqRu',
		),
	),
	users : array(
		$client->userEmpty(
			id : 5321526343997084254,
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
			id : 9192100746801015684,
			access_hash : -237850158695882496,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 47,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'a6iglsQjXpL7SxGr',
					reason : 'DIErWkMxvuVHT5B4',
					text : 'qpBPuN1iE9rlLyFX',
				),
			),
			bot_inline_placeholder : 'smyLZCVBtOGzjJxM',
			lang_code : 'pqEUARZuDWX9zjx1',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 68,
			color : $client->peerColor(
				color : 36,
				background_emoji_id : -1288707789583860009,
			),
			profile_color : $client->peerColor(
				color : 88,
				background_emoji_id : 8305929298946320455,
			),
			bot_active_users : 56,
			bot_verification_icon : -4707360951903231604,
			send_paid_messages_stars : -7858791121560476153,
		),
	),
);
```