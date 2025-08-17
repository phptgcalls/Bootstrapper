# inputGroupCall

**Description** : *Points to a specific group call*

**Layer** : 211

```tl
inputGroupCall#d8aa840f id:long access_hash:long = InputGroupCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Group call ID |
| <mark>access_hash</mark> | [`long`](type/long) | Group call access hash |

---

## Type

[InputGroupCall](type/InputGroupCall)

---

## Example

```php
$inputGroupCall = $client->inputGroupCall(
	id : -3216598881515966513,
	access_hash : 6021734753479130014,
);
```