# paymentSavedCredentialsCard

**Description** : *Saved credit card*

**Layer** : 211

```tl
paymentSavedCredentialsCard#cdc27a1f id:string title:string = PaymentSavedCredentials;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`string`](type/string) | Card ID |
| <mark>title</mark> | [`string`](type/string) | Title |

---

## Type

[PaymentSavedCredentials](type/PaymentSavedCredentials)

---

## Example

```php
$paymentSavedCredentials = $client->paymentSavedCredentialsCard(
	id : 'EApHZnzF04ldeQou',
	title : 'rzyVAiW84mkpFnsq',
);
```