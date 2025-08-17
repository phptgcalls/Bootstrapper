# notificationSoundRingtone

**Description** : *A specific previously uploaded notification sound should be used*

**Layer** : 211

```tl
notificationSoundRingtone#ff6c8049 id:long = NotificationSound;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`long`](type/long) | Document ID of notification sound uploaded using account.uploadRingtone |

---

## Type

[NotificationSound](type/NotificationSound)

---

## Example

```php
$notificationSound = $client->notificationSoundRingtone(
	id : -1120687139215118170,
);
```