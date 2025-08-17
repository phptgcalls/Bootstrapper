# auth.authorization

**Description** : *Contains user authorization info*

**Layer** : 211

```tl
auth.authorization#2ea2c0d4 flags:# setup_password_required:flags.1?true otherwise_relogin_days:flags.1?int tmp_sessions:flags.0?int future_auth_token:flags.2?bytes user:User = auth.Authorization;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **setup_password_required** | [`flags.1?true`](type/true) | Suggests the user to set up a 2-step verification password to be able to log in again |
| **otherwise_relogin_days** | [`flags.1?int`](type/int) | Iff setup_password_required is set and the user declines to set a 2-step verification password, they will be able to log into their account via SMS again only after this many days pass |
| **tmp_sessions** | [`flags.0?int`](type/int) | Temporary passport sessions |
| **future_auth_token** | [`flags.2?bytes`](type/bytes) | A future auth token |
| <mark>user</mark> | [`User`](type/User) | Info on authorized user |

---

## Type

[auth.Authorization](type/auth.Authorization)

---

## Example

```php
$authAuthorization = $client->auth->authorization(
	setup_password_required : true,
	otherwise_relogin_days : 15,
	tmp_sessions : 94,
	future_auth_token : '7=??LiveProto?!' . "\0" . '??',
	user : $client->userEmpty(
		id : 1934335622729983009,
	),
);
```