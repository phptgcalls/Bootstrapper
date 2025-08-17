# updateBotShippingQuery

**Description** : *This object contains information about an incoming shipping query*

**Layer** : 211

```tl
updateBotShippingQuery#b5aefd7d query_id:long user_id:long payload:bytes shipping_address:PostAddress = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>query_id</mark> | [`long`](type/long) | Unique query identifier |
| <mark>user_id</mark> | [`long`](type/long) | User who sent the query |
| <mark>payload</mark> | [`bytes`](type/bytes) | Bot specified invoice payload |
| <mark>shipping_address</mark> | [`PostAddress`](type/PostAddress) | User specified shipping address |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotShippingQuery(
	query_id : 6452980343199364296,
	user_id : 8033166513352840198,
	payload : ']??Y?LiveProtou???',
	shipping_address : $client->postAddress(
		street_line1 : 'agI5c0W7fkFyoPbR',
		street_line2 : 'OrXYw4v3DRMVZQ5i',
		city : '78UQbtgkWFliumKc',
		state : 'qunltd03xiWeSEjk',
		country_iso2 : 'b8ICHMJcSEpVXtyT',
		post_code : 'EW8SFkIKoxgv3z04',
	),
);
```