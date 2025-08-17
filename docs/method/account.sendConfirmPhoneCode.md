# account.sendConfirmPhoneCode

**Description** : *Send confirmation code to cancel account deletion, for more info click here »*

**Layer** : 211

```tl
account.sendConfirmPhoneCode#1b3faa88 hash:string settings:CodeSettings = auth.SentCode;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`string`](type/string) | The hash from the service notification, for more info click here » |
| <mark>settings</mark> | [`CodeSettings`](type/CodeSettings) | Phone code settings |

---

## Result

[auth.SentCode](type/auth.SentCode)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **HASH_INVALID** | `400` | The provided hash is invalid |

---

## Example

```php
$authSentCode = $client->account->sendConfirmPhoneCode(
	hash : 'p9wqjAxEaMob5fd3',
	settings : $client->codeSettings(
		allow_flashcall : true,
		current_number : true,
		allow_app_hash : true,
		allow_missed_call : true,
		allow_firebase : true,
		unknown_number : true,
		logout_tokens : array('?I\\/sLiveProto??p?2'),
		token : 'ZBnv3w1uWFP6imtp',
		app_sandbox : $client->boolFalse(),
	),
);
```