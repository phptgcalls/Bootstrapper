# updateChatParticipants

**Description** : *Composition of chat participants changed*

**Layer** : 211

```tl
updateChatParticipants#7761198 participants:ChatParticipants = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>participants</mark> | [`ChatParticipants`](type/ChatParticipants) | Updated chat participants |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateChatParticipants(
	participants : $client->chatParticipantsForbidden(
		chat_id : -1227918849564120267,
		self_participant : $client->chatParticipant(
			user_id : -6215020289892517183,
			inviter_id : -8383079451286384589,
			date : 53,
		),
	),
);
```