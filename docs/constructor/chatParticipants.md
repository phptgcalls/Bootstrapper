# chatParticipants

**Description** : *Group members*

**Layer** : 211

```tl
chatParticipants#3cbc93f8 chat_id:long participants:Vector<ChatParticipant> version:int = ChatParticipants;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chat_id</mark> | [`long`](type/long) | Group identifier |
| <mark>participants</mark> | [`Vector<ChatParticipant>`](type/ChatParticipant) | List of group members |
| <mark>version</mark> | [`int`](type/int) | Group version number |

---

## Type

[ChatParticipants](type/ChatParticipants)

---

## Example

```php
$chatParticipants = $client->chatParticipants(
	chat_id : -1305867419510180639,
	participants : array(
		$client->chatParticipant(
			user_id : 6359201200541711501,
			inviter_id : -770157131821741536,
			date : 85,
		),
		$client->chatParticipantCreator(
			user_id : -3071873895504692715,
		),
		$client->chatParticipantAdmin(
			user_id : -2410226064222715579,
			inviter_id : 2975101093890538115,
			date : 4,
		),
	),
	version : 49,
);
```