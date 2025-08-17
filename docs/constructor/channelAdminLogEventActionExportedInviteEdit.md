# channelAdminLogEventActionExportedInviteEdit

**Description** : *A chat invite was edited*

**Layer** : 211

```tl
channelAdminLogEventActionExportedInviteEdit#e90ebb59 prev_invite:ExportedChatInvite new_invite:ExportedChatInvite = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>prev_invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | Previous chat invite information |
| <mark>new_invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | New chat invite information |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionExportedInviteEdit(
	prev_invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : '5lahEtJjWqrG37oS',
		admin_id : 7930925315691389993,
		date : 6,
		start_date : 58,
		expire_date : 85,
		usage_limit : 90,
		usage : 34,
		requested : 36,
		subscription_expired : 27,
		title : 'IPNsbiWhvLlBGKrw',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 18,
			amount : 8877732975531443095,
		),
	),
	new_invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'BUhj0FrDvHbNfMqR',
		admin_id : 6238056685926020083,
		date : 64,
		start_date : 71,
		expire_date : 29,
		usage_limit : 76,
		usage : 74,
		requested : 11,
		subscription_expired : 93,
		title : '5Y2DPpBMRF4xyqQV',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 52,
			amount : 7353195378274807722,
		),
	),
);
```