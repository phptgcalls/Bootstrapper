# auth.dropTempAuthKeys

**Description** : *Delete all temporary authorization keys except for the ones specified*

**Layer** : 211

```tl
auth.dropTempAuthKeys#8e48a188 except_auth_keys:Vector<long> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>except_auth_keys</mark> | [`Vector<long>`](type/long) | The auth keys that shouldn't be dropped |

---

## Result

[Bool](type/Bool)

---

## Example

```php
$bool = $client->auth->dropTempAuthKeys(
	except_auth_keys : array(4595403781437581429),
);
```