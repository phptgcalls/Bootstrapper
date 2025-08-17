# updateChatParticipant

**Description** : *A user has joined or left a specific chat*

**Layer** : 211

```tl
updateChatParticipant#d087663a flags:# chat_id:long date:int actor_id:long user_id:long prev_participant:flags.0?ChatParticipant new_participant:flags.1?ChatParticipant invite:flags.2?ExportedChatInvite qts:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>chat_id</mark> | [`long`](type/long) | Chat ID |
| <mark>date</mark> | [`int`](type/int) | When did this event occur |
| <mark>actor_id</mark> | [`long`](type/long) | User that triggered the change (inviter, admin that kicked the user, or the even the user_id itself) |
| <mark>user_id</mark> | [`long`](type/long) | User that was affected by the change |
| **prev_participant** | [`flags.0?ChatParticipant`](type/ChatParticipant) | Previous participant info (empty if this participant just joined) |
| **new_participant** | [`flags.1?ChatParticipant`](type/ChatParticipant) | New participant info (empty if this participant just left) |
| **invite** | [`flags.2?ExportedChatInvite`](type/ExportedChatInvite) | The invite that was used to join the group |
| <mark>qts</mark> | [`int`](type/int) | New qts value, see updates » for more info |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateChatParticipant(
	chat_id : -6216960492759684642,
	date : 14,
	actor_id : 7515182994764432489,
	user_id : 5360413689913343012,
	prev_participant : $client->chatParticipant(
		user_id : 4679123567436788165,
		inviter_id : 6971488629877814505,
		date : 13,
	),
	new_participant : $client->chatParticipant(
		user_id : 8879579534362341063,
		inviter_id : 5035132780988278710,
		date : 79,
	),
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'JNLUcRzrCGlsIo96',
		admin_id : -1353185296725144302,
		date : 5,
		start_date : 41,
		expire_date : 73,
		usage_limit : 62,
		usage : 84,
		requested : 67,
		subscription_expired : 39,
		title : 'CwEld7bgOQhAM4fo',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 47,
			amount : 7134237215524591627,
		),
	),
	qts : 32,
);
```