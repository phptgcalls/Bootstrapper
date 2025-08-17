# passwordKdfAlgoSHA256SHA256PBKDF2HMACSHA512iter100000SHA256ModPow

**Description** : *This key derivation algorithm defines that SRP 2FA login must be used*

**Layer** : 211

```tl
passwordKdfAlgoSHA256SHA256PBKDF2HMACSHA512iter100000SHA256ModPow#3a912d4a salt1:bytes salt2:bytes g:int p:bytes = PasswordKdfAlgo;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>salt1</mark> | [`bytes`](type/bytes) | One of two salts used by the derivation function (see SRP 2FA login) |
| <mark>salt2</mark> | [`bytes`](type/bytes) | One of two salts used by the derivation function (see SRP 2FA login) |
| <mark>g</mark> | [`int`](type/int) | Base (see SRP 2FA login) |
| <mark>p</mark> | [`bytes`](type/bytes) | 2048-bit modulus (see SRP 2FA login) |

---

## Type

[PasswordKdfAlgo](type/PasswordKdfAlgo)

---

## Example

```php
$passwordKdfAlgo = $client->passwordKdfAlgoSHA256SHA256PBKDF2HMACSHA512iter100000SHA256ModPow(
	salt1 : '?K	`?LiveProto?????',
	salt2 : '?L.^LiveProto??I??',
	g : 61,
	p : 'T??f?LiveProto??op',
);
```