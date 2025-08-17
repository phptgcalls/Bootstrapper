# inputStorePaymentStarsTopup

**Description** : *Used to top up the Telegram Stars balance of the current account*

**Layer** : 211

```tl
inputStorePaymentStarsTopup#dddd0f56 stars:long currency:string amount:long = InputStorePaymentPurpose;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>stars</mark> | [`long`](type/long) | Amount of stars to topup |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code |
| <mark>amount</mark> | [`long`](type/long) | Total price in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |

---

## Type

[InputStorePaymentPurpose](type/InputStorePaymentPurpose)

---

## Example

```php
$inputStorePaymentPurpose = $client->inputStorePaymentStarsTopup(
	stars : -7347745538482921861,
	currency : 'eJy4Sx7XYO5jBK6k',
	amount : -2478347279597432706,
);
```