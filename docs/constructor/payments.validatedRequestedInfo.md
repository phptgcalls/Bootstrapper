# payments.validatedRequestedInfo

**Description** : *Validated user-provided info*

**Layer** : 211

```tl
payments.validatedRequestedInfo#d1451883 flags:# id:flags.0?string shipping_options:flags.1?Vector<ShippingOption> = payments.ValidatedRequestedInfo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **id** | [`flags.0?string`](type/string) | ID |
| **shipping_options** | [`flags.1?Vector<ShippingOption>`](type/ShippingOption) | Shipping options |

---

## Type

[payments.ValidatedRequestedInfo](type/payments.ValidatedRequestedInfo)

---

## Example

```php
$paymentsValidatedRequestedInfo = $client->payments->validatedRequestedInfo(
	id : 'Yhcb2eWC6inSMDxp',
	shipping_options : array(
		$client->shippingOption(
			id : 'pKWDTe6bX4Oga5M1',
			title : 'HBYIUqfhTkz3D9am',
			prices : array(
				$client->labeledPrice(
					label : 'FU1AfghKtWVx6var',
					amount : 1960921289208721838,
				),
			),
		),
	),
);
```