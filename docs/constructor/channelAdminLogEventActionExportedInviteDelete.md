# channelAdminLogEventActionExportedInviteDelete

**Description** : *A chat invite was deleted*

**Layer** : 211

```tl
channelAdminLogEventActionExportedInviteDelete#5a50fca4 invite:ExportedChatInvite = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | The deleted chat invite |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionExportedInviteDelete(
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'ACZXnwcVy9pS3JFG',
		admin_id : 3378066179401712886,
		date : 61,
		start_date : 47,
		expire_date : 43,
		usage_limit : 79,
		usage : 34,
		requested : 72,
		subscription_expired : 60,
		title : '5omqLZbWUaAOPGDh',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 66,
			amount : 6063052394583270827,
		),
	),
);
```