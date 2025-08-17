# messageActionGiftTon

**Layer** : 211

```tl
messageActionGiftTon#a8a3c699 flags:# currency:string amount:long crypto_currency:string crypto_amount:long transaction_id:flags.0?string = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| <mark>currency</mark> | [`string`](type/string) | NOTHING |
| <mark>amount</mark> | [`long`](type/long) | NOTHING |
| <mark>crypto_currency</mark> | [`string`](type/string) | NOTHING |
| <mark>crypto_amount</mark> | [`long`](type/long) | NOTHING |
| **transaction_id** | [`flags.0?string`](type/string) | NOTHING |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionGiftTon(
	currency : 'ahnVtlqUc06siMNk',
	amount : 2239266076037460031,
	crypto_currency : 'Fv6l15GoCW0MyaYk',
	crypto_amount : -441226015336052016,
	transaction_id : 'CZ8MiPKlqRtVa5Sv',
);
```