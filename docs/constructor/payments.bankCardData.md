# payments.bankCardData

**Description** : *Credit card info, provided by the card's bank(s)*

**Layer** : 211

```tl
payments.bankCardData#3e24e573 title:string open_urls:Vector<BankCardOpenUrl> = payments.BankCardData;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>title</mark> | [`string`](type/string) | Credit card title |
| <mark>open_urls</mark> | [`Vector<BankCardOpenUrl>`](type/BankCardOpenUrl) | Info URL(s) provided by the card's bank(s) |

---

## Type

[payments.BankCardData](type/payments.BankCardData)

---

## Example

```php
$paymentsBankCardData = $client->payments->bankCardData(
	title : 'QbJOlXIPMkjVUNzB',
	open_urls : array(
		$client->bankCardOpenUrl(
			url : 'https://docs.liveproto.dev',
			name : 'cXZNrh0PCvQJHt6w',
		),
	),
);
```