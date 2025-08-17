# updateBotPrecheckoutQuery

**Description** : *This object contains information about an incoming pre-checkout query*

**Layer** : 211

```tl
updateBotPrecheckoutQuery#8caa9a96 flags:# query_id:long user_id:long payload:bytes info:flags.0?PaymentRequestedInfo shipping_option_id:flags.1?string currency:string total_amount:long = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>query_id</mark> | [`long`](type/long) | Unique query identifier |
| <mark>user_id</mark> | [`long`](type/long) | User who sent the query |
| <mark>payload</mark> | [`bytes`](type/bytes) | Bot specified invoice payload |
| **info** | [`flags.0?PaymentRequestedInfo`](type/PaymentRequestedInfo) | Order info provided by the user |
| **shipping_option_id** | [`flags.1?string`](type/string) | Identifier of the shipping option chosen by the user |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code, or XTR for Telegram Stars |
| <mark>total_amount</mark> | [`long`](type/long) | Total amount in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotPrecheckoutQuery(
	query_id : 3181990008964569306,
	user_id : -6806585356563086559,
	payload : '?j?}LiveProto$??0?',
	info : $client->paymentRequestedInfo(
		name : '3DRBxG7Yh5y2W6kO',
		phone : '+1234567890',
		email : 'reply@liveproto.dev',
		shipping_address : $client->postAddress(
			street_line1 : 'HPX3MQ5VwWJaxZBn',
			street_line2 : 'B27OaPK5L4NTdx6n',
			city : 'UOveM8ucjK6D7ZBl',
			state : 'wPTGsb2LNQKFpBID',
			country_iso2 : 'Fbu0RaVhIPvioyct',
			post_code : '6DfvZRmasejKd32L',
		),
	),
	shipping_option_id : 'zxMsnrVABkS4CITH',
	currency : 'R0NjWhMxpTiVlPJD',
	total_amount : 3250928891918802699,
);
```