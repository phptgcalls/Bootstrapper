# channelAdminLogEventActionParticipantInvite

**Description** : *A user was invited to the group*

**Layer** : 211

```tl
channelAdminLogEventActionParticipantInvite#e31c34d8 participant:ChannelParticipant = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>participant</mark> | [`ChannelParticipant`](type/ChannelParticipant) | The user that was invited |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionParticipantInvite(
	participant : $client->channelParticipant(
		user_id : -3961150427108589814,
		date : 37,
		subscription_until_date : 47,
	),
);
```