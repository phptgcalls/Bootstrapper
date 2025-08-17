# starsSubscription

**Description** : *Represents a Telegram Star subscription »*

**Layer** : 211

```tl
starsSubscription#2e6eab1a flags:# canceled:flags.0?true can_refulfill:flags.1?true missing_balance:flags.2?true bot_canceled:flags.7?true id:string peer:Peer until_date:int pricing:StarsSubscriptionPricing chat_invite_hash:flags.3?string title:flags.4?string photo:flags.5?WebDocument invoice_slug:flags.6?string = StarsSubscription;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **canceled** | [`flags.0?true`](type/true) | Whether this subscription was cancelled |
| **can_refulfill** | [`flags.1?true`](type/true) | Whether we left the associated private channel, but we can still rejoin it using payments.fulfillStarsSubscription because the current subscription period hasn't expired yet |
| **missing_balance** | [`flags.2?true`](type/true) | Whether this subscription has expired because there are not enough stars on the user's balance to extend it |
| **bot_canceled** | [`flags.7?true`](type/true) | Set if this bot subscription was cancelled by the bot |
| <mark>id</mark> | [`string`](type/string) | Subscription ID |
| <mark>peer</mark> | [`Peer`](type/Peer) | Identifier of the associated private chat |
| <mark>until_date</mark> | [`int`](type/int) | Expiration date of the current subscription period |
| <mark>pricing</mark> | [`StarsSubscriptionPricing`](type/StarsSubscriptionPricing) | Pricing of the subscription in Telegram Stars |
| **chat_invite_hash** | [`flags.3?string`](type/string) | Invitation link, used to renew the subscription after cancellation or expiration |
| **title** | [`flags.4?string`](type/string) | For bot subscriptions, the title of the subscription invoice |
| **photo** | [`flags.5?WebDocument`](type/WebDocument) | For bot subscriptions, the photo from the subscription invoice |
| **invoice_slug** | [`flags.6?string`](type/string) | For bot subscriptions, the identifier of the subscription invoice |

---

## Type

[StarsSubscription](type/StarsSubscription)

---

## Example

```php
$starsSubscription = $client->starsSubscription(
	canceled : true,
	can_refulfill : true,
	missing_balance : true,
	bot_canceled : true,
	id : 'GAjDqeJuKLcRsxrO',
	peer : $client->peerUser(
		user_id : -7429955669671849863,
	),
	until_date : 81,
	pricing : $client->starsSubscriptionPricing(
		period : 40,
		amount : 2954072858646984475,
	),
	chat_invite_hash : 'Qjo7LBsVGKlkSDZt',
	title : 'W8LzcVtCXuISmZap',
	photo : $client->webDocument(
		url : 'https://docs.liveproto.dev',
		access_hash : -4859877310190233521,
		size : 8,
		mime_type : 'Ozgs6fDdEvp3joRi',
		attributes : array(
			$client->documentAttributeImageSize(
				w : 70,
				h : 57,
			),
			$client->documentAttributeAnimated(),
			$client->documentAttributeSticker(
				mask : true,
				alt : 'Xf23t1IADQFNhgmU',
				stickerset : $client->inputStickerSetEmpty(...),
				mask_coords : $client->maskCoords(...),
			),
			$client->documentAttributeVideo(
				round_message : true,
				supports_streaming : true,
				nosound : true,
				duration : -468446.580078125,
				w : 86,
				h : 39,
				preload_prefix_size : 87,
				video_start_ts : 639526.01171875,
				video_codec : 'rRsqwPEtczpXfxGS',
			),
			$client->documentAttributeAudio(
				voice : true,
				duration : 80,
				title : '4XdBVoOzQc1sxmSP',
				performer : 'fogXVKI5Ut6M2lhB',
				waveform : '.??LiveProto??{',
			),
			$client->documentAttributeFilename(
				file_name : 'BG5wvAzxLFZa4uEQ',
			),
			$client->documentAttributeHasStickers(),
			$client->documentAttributeCustomEmoji(
				free : true,
				text_color : true,
				alt : '3ktDNAqraKSUGTlz',
				stickerset : $client->inputStickerSetEmpty(...),
			),
		),
	),
	invoice_slug : 'Blz0Fij5YRgbGUIT',
);
```