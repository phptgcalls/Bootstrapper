# inputPhoneCall

**Description** : *Phone call*

**Layer** : 211

```tl
inputPhoneCall#1e36fded id:long access_hash:long = InputPhoneCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Call ID |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash |

---

## Type

[InputPhoneCall](type/InputPhoneCall)

---

## Example

```php
$inputPhoneCall = $client->inputPhoneCall(
	id : -3836743150749728883,
	access_hash : 8255353307221705361,
);
```