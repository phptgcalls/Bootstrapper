# auth.loginToken

**Description** : *Login token (for QR code login)*

**Layer** : 211

```tl
auth.loginToken#629f1980 expires:int token:bytes = auth.LoginToken;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>expires</mark> | [`int`](type/int) | Expiration date of QR code |
| <mark>token</mark> | [`bytes`](type/bytes) | Token to render in QR code |

---

## Type

[auth.LoginToken](type/auth.LoginToken)

---

## Example

```php
$authLoginToken = $client->auth->loginToken(
	expires : 57,
	token : 'Θ???LiveProto`?O??',
);
```