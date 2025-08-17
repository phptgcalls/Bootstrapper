# inputInvoiceBusinessBotTransferStars

**Layer** : 211

```tl
inputInvoiceBusinessBotTransferStars#f4997e42 bot:InputUser stars:long = InputInvoice;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>bot</mark> | [`InputUser`](type/InputUser) | NOTHING |
| <mark>stars</mark> | [`long`](type/long) | NOTHING |

---

## Type

[InputInvoice](type/InputInvoice)

---

## Example

```php
$inputInvoice = $client->inputInvoiceBusinessBotTransferStars(
	bot : $client->inputUserEmpty(),
	stars : -5972755878385988657,
);
```