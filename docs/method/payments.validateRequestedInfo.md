# payments.validateRequestedInfo

**Description** : *Submit requested order information for validation*

**Layer** : 211

```tl
payments.validateRequestedInfo#b6c8f12b flags:# save:flags.0?true invoice:InputInvoice info:PaymentRequestedInfo = payments.ValidatedRequestedInfo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **save** | [`flags.0?true`](type/true) | Save order information to re-use it for future orders |
| <mark>invoice</mark> | [`InputInvoice`](type/InputInvoice) | Invoice |
| <mark>info</mark> | [`PaymentRequestedInfo`](type/PaymentRequestedInfo) | Requested order information |

---

## Result

[payments.ValidatedRequestedInfo](type/payments.ValidatedRequestedInfo)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **MESSAGE_ID_INVALID** | `400` | The provided message id is invalid |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$paymentsValidatedRequestedInfo = $client->payments->validateRequestedInfo(
	save : true,
	invoice : $client->inputInvoiceMessage(
		peer : $client->inputPeerEmpty(),
		msg_id : 27,
	),
	info : $client->paymentRequestedInfo(
		name : 'woSNXn75d8L3lfKy',
		phone : '+1234567890',
		email : 'reply@liveproto.dev',
		shipping_address : $client->postAddress(
			street_line1 : 'NoUbfjcGxPav2klZ',
			street_line2 : '3xBJXNKAM4qyncs2',
			city : '6eAFVd1rZhIUa7P5',
			state : 'M9fwN3vpLqoAnzXR',
			country_iso2 : 'dbg0DhT7zeBG5SNc',
			post_code : 'ptcxkUOJidRBXl5r',
		),
	),
);
```