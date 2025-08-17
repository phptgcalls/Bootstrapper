# emailVerificationCode

**Description** : *Email verification code*

**Layer** : 211

```tl
emailVerificationCode#922e55a9 code:string = EmailVerification;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>code</mark> | [`string`](type/string) | Received verification code |

---

## Type

[EmailVerification](type/EmailVerification)

---

## Example

```php
$emailVerification = $client->emailVerificationCode(
	code : 'iCR2Qfo6OmakJS0L',
);
```