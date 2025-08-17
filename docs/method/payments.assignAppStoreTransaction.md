# payments.assignAppStoreTransaction

**Description** : *Informs server about a purchase made through the App Store: for official applications only*

**Layer** : 211

```tl
payments.assignAppStoreTransaction#80ed747d receipt:bytes purpose:InputStorePaymentPurpose = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>receipt</mark> | [`bytes`](type/bytes) | Receipt |
| <mark>purpose</mark> | [`InputStorePaymentPurpose`](type/InputStorePaymentPurpose) | Payment purpose |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **RECEIPT_EMPTY** | `400` | The specified receipt is empty |

---

## Example

```php
$updates = $client->payments->assignAppStoreTransaction(
	receipt : 'L??LiveProto?VPr',
	purpose : $client->inputStorePaymentPremiumSubscription(
		restore : true,
		upgrade : true,
	),
);
```