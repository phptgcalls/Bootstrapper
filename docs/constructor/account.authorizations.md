# account.authorizations

**Description** : *Logged-in sessions*

**Layer** : 211

```tl
account.authorizations#4bff8ea0 authorization_ttl_days:int authorizations:Vector<Authorization> = account.Authorizations;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>authorization_ttl_days</mark> | [`int`](type/int) | Time-to-live of session |
| <mark>authorizations</mark> | [`Vector<Authorization>`](type/Authorization) | Logged-in sessions |

---

## Type

[account.Authorizations](type/account.Authorizations)

---

## Example

```php
$accountAuthorizations = $client->account->authorizations(
	authorization_ttl_days : 52,
	authorizations : array(
		$client->authorization(
			current : true,
			official_app : true,
			password_pending : true,
			encrypted_requests_disabled : true,
			call_requests_disabled : true,
			unconfirmed : true,
			hash : 4413023476180975515,
			device_model : 'ZxywKmFl1RN9VDqr',
			platform : 'o2HmBXY7ed8QEp9n',
			system_version : 'ti2RQgpoKmJGCdOh',
			api_id : 29,
			app_name : 'dghIAxyHZmw5i7RN',
			app_version : 'wdGAcM01Olq32SCQ',
			date_created : 5,
			date_active : 58,
			ip : '127.0.0.1',
			country : 'eQYLncS1zwBloaPy',
			region : 'c3iaynbDNC9UxJzh',
		),
	),
);
```