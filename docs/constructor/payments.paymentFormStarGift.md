# payments.paymentFormStarGift

**Description** : *Represents a payment form for a gift, see here » for more info*

**Layer** : 211

```tl
payments.paymentFormStarGift#b425cfe1 form_id:long invoice:Invoice = payments.PaymentForm;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>form_id</mark> | [`long`](type/long) | Form ID |
| <mark>invoice</mark> | [`Invoice`](type/Invoice) | Invoice |

---

## Type

[payments.PaymentForm](type/payments.PaymentForm)

---

## Example

```php
$paymentsPaymentForm = $client->payments->paymentFormStarGift(
	form_id : -6615928347376697000,
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
		currency : 'GnVR0yjEa4KqONM2',
		prices : array(
			$client->labeledPrice(
				label : 'R6dOfnWugGaEU9ze',
				amount : 2276013570897184998,
			),
		),
		max_tip_amount : 7781275146337250073,
		suggested_tip_amounts : array(-2139888582561202235),
		terms_url : 'https://docs.liveproto.dev',
		subscription_period : 36,
	),
);
```