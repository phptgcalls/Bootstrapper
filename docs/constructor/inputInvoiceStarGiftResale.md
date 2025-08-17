# inputInvoiceStarGiftResale

**Layer** : 211

```tl
inputInvoiceStarGiftResale#c39f5324 flags:# ton:flags.0?true slug:string to_id:InputPeer = InputInvoice;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **ton** | [`flags.0?true`](type/true) | NOTHING |
| <mark>slug</mark> | [`string`](type/string) | NOTHING |
| <mark>to_id</mark> | [`InputPeer`](type/InputPeer) | NOTHING |

---

## Type

[InputInvoice](type/InputInvoice)

---

## Example

```php
$inputInvoice = $client->inputInvoiceStarGiftResale(
	ton : true,
	slug : 'Q6azw4GO2RpWts5b',
	to_id : $client->inputPeerEmpty(),
);
```