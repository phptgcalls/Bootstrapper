# chatParticipant

**Description** : *Group member*

**Layer** : 211

```tl
chatParticipant#c02d4007 user_id:long inviter_id:long date:int = ChatParticipant;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>user_id</mark> | [`long`](type/long) | Member user ID |
| <mark>inviter_id</mark> | [`long`](type/long) | ID of the user that added the member to the group |
| <mark>date</mark> | [`int`](type/int) | Date added to the group |

---

## Type

[ChatParticipant](type/ChatParticipant)

---

## Example

```php
$chatParticipant = $client->chatParticipant(
	user_id : 5187139421554744147,
	inviter_id : -7766878662005186794,
	date : 67,
);
```