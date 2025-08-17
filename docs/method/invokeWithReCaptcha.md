# invokeWithReCaptcha

**Layer** : 211

```tl
invokeWithReCaptcha#adbb0f94 {X:Type} token:string query:!X = X;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>token</mark> | [`string`](type/string) | NOTHING |
| <mark>query</mark> | [`!X`](type/X) | NOTHING |

---

## Result

[X](type/X)

---

## Example

```php
$x = $client->invokeWithReCaptcha(
	token : 'SMtudjKm27FW1xaV',
	query : $client->X(),
);
```