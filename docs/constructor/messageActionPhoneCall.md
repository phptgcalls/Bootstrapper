# messageActionPhoneCall

**Description** : *A phone call*

**Layer** : 211

```tl
messageActionPhoneCall#80e11a7f flags:# video:flags.2?true call_id:long reason:flags.0?PhoneCallDiscardReason duration:flags.1?int = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **video** | [`flags.2?true`](type/true) | Is this a video call? |
| <mark>call_id</mark> | [`long`](type/long) | Call ID |
| **reason** | [`flags.0?PhoneCallDiscardReason`](type/PhoneCallDiscardReason) | If the call has ended, the reason why it ended |
| **duration** | [`flags.1?int`](type/int) | Duration of the call in seconds |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionPhoneCall(
	video : true,
	call_id : 1102986280733774240,
	reason : $client->phoneCallDiscardReasonMissed(),
	duration : 81,
);
```