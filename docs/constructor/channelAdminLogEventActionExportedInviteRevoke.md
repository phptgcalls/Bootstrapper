# channelAdminLogEventActionExportedInviteRevoke

**Description** : *A specific invite link was revoked*

**Layer** : 211

```tl
channelAdminLogEventActionExportedInviteRevoke#410a134e invite:ExportedChatInvite = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | The invite link that was revoked |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionExportedInviteRevoke(
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'gU7zMFlbjrY318co',
		admin_id : 8459346554786027993,
		date : 65,
		start_date : 75,
		expire_date : 48,
		usage_limit : 43,
		usage : 74,
		requested : 97,
		subscription_expired : 5,
		title : 'QyCRvcZo3dbfpMzO',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 80,
			amount : -790347641184049490,
		),
	),
);
```