# invoice

**Description** : *Invoice*

**Layer** : 211

```tl
invoice#49ee584 flags:# test:flags.0?true name_requested:flags.1?true phone_requested:flags.2?true email_requested:flags.3?true shipping_address_requested:flags.4?true flexible:flags.5?true phone_to_provider:flags.6?true email_to_provider:flags.7?true recurring:flags.9?true currency:string prices:Vector<LabeledPrice> max_tip_amount:flags.8?long suggested_tip_amounts:flags.8?Vector<long> terms_url:flags.10?string subscription_period:flags.11?int = Invoice;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **test** | [`flags.0?true`](type/true) | Test invoice |
| **name_requested** | [`flags.1?true`](type/true) | Set this flag if you require the user's full name to complete the order |
| **phone_requested** | [`flags.2?true`](type/true) | Set this flag if you require the user's phone number to complete the order |
| **email_requested** | [`flags.3?true`](type/true) | Set this flag if you require the user's email address to complete the order |
| **shipping_address_requested** | [`flags.4?true`](type/true) | Set this flag if you require the user's shipping address to complete the order |
| **flexible** | [`flags.5?true`](type/true) | Set this flag if the final price depends on the shipping method |
| **phone_to_provider** | [`flags.6?true`](type/true) | Set this flag if user's phone number should be sent to provider |
| **email_to_provider** | [`flags.7?true`](type/true) | Set this flag if user's email address should be sent to provider |
| **recurring** | [`flags.9?true`](type/true) | Whether this is a recurring payment |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code, or XTR for Telegram Stars |
| <mark>prices</mark> | [`Vector<LabeledPrice>`](type/LabeledPrice) | Price breakdown, a list of components (e.g. product price, tax, discount, delivery cost, delivery tax, bonus, etc.) |
| **max_tip_amount** | [`flags.8?long`](type/long) | The maximum accepted amount for tips in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |
| **suggested_tip_amounts** | [`flags.8?Vector<long>`](type/long) | A vector of suggested amounts of tips in the smallest units of the currency (integer, not float/double). At most 4 suggested tip amounts can be specified. The suggested tip amounts must be positive, passed in a strictly increased order and must not exceed max_tip_amount |
| **terms_url** | [`flags.10?string`](type/string) | Terms of service URL |
| **subscription_period** | [`flags.11?int`](type/int) | The number of seconds between consecutive Telegram Star debiting for bot subscription invoices |

---

## Type

[Invoice](type/Invoice)

---

## Example

```php
$invoice = $client->invoice(
	test : true,
	name_requested : true,
	phone_requested : true,
	email_requested : true,
	shipping_address_requested : true,
	flexible : true,
	phone_to_provider : true,
	email_to_provider : true,
	recurring : true,
	currency : 'r1iMPhk7tGzVUycm',
	prices : array(
		$client->labeledPrice(
			label : 'e5xnpFT1QS3Ob6lM',
			amount : 3436036748436874732,
		),
	),
	max_tip_amount : 3124812373340580485,
	suggested_tip_amounts : array(5883143129005294477),
	terms_url : 'https://docs.liveproto.dev',
	subscription_period : 97,
);
```