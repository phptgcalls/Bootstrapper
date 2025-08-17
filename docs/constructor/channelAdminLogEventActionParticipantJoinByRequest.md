# channelAdminLogEventActionParticipantJoinByRequest

**Description** : *A new member was accepted to the chat by an admin*

**Layer** : 211

```tl
channelAdminLogEventActionParticipantJoinByRequest#afb6144a invite:ExportedChatInvite approved_by:long = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | The invite link that was used to join the chat |
| <mark>approved_by</mark> | [`long`](type/long) | ID of the admin that approved the invite |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionParticipantJoinByRequest(
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'yNXj4MVeBYatToQz',
		admin_id : 1418247138540908496,
		date : 7,
		start_date : 47,
		expire_date : 24,
		usage_limit : 83,
		usage : 34,
		requested : 32,
		subscription_expired : 100,
		title : 'Se05KfXuIbvJshVE',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 65,
			amount : 5608397021275820991,
		),
	),
	approved_by : -5476350551930375257,
);
```