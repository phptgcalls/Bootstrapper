# chatInviteImporter

**Description** : *When and which user joined the chat using a chat invite*

**Layer** : 211

```tl
chatInviteImporter#8c5adfd9 flags:# requested:flags.0?true via_chatlist:flags.3?true user_id:long date:int about:flags.2?string approved_by:flags.1?long = ChatInviteImporter;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **requested** | [`flags.0?true`](type/true) | Whether this user currently has a pending join request » |
| **via_chatlist** | [`flags.3?true`](type/true) | The participant joined by importing a chat folder deep link » |
| <mark>user_id</mark> | [`long`](type/long) | The user |
| <mark>date</mark> | [`int`](type/int) | When did the user join |
| **about** | [`flags.2?string`](type/string) | For users with pending requests, contains bio of the user that requested to join |
| **approved_by** | [`flags.1?long`](type/long) | The administrator that approved the join request » of the user |

---

## Type

[ChatInviteImporter](type/ChatInviteImporter)

---

## Example

```php
$chatInviteImporter = $client->chatInviteImporter(
	requested : true,
	via_chatlist : true,
	user_id : -1240831842501481560,
	date : 71,
	about : '4zGLBkJFinQc1y0X',
	approved_by : -6998525308602188312,
);
```