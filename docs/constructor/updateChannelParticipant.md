# updateChannelParticipant

**Description** : *A participant has left, joined, was banned or admined in a channel or supergroup*

**Layer** : 211

```tl
updateChannelParticipant#985d3abb flags:# via_chatlist:flags.3?true channel_id:long date:int actor_id:long user_id:long prev_participant:flags.0?ChannelParticipant new_participant:flags.1?ChannelParticipant invite:flags.2?ExportedChatInvite qts:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **via_chatlist** | [`flags.3?true`](type/true) | Whether the participant joined using a chat folder deep link » |
| <mark>channel_id</mark> | [`long`](type/long) | Channel ID |
| <mark>date</mark> | [`int`](type/int) | Date of the event |
| <mark>actor_id</mark> | [`long`](type/long) | User that triggered the change (inviter, admin that kicked the user, or the even the user_id itself) |
| <mark>user_id</mark> | [`long`](type/long) | User that was affected by the change |
| **prev_participant** | [`flags.0?ChannelParticipant`](type/ChannelParticipant) | Previous participant status |
| **new_participant** | [`flags.1?ChannelParticipant`](type/ChannelParticipant) | New participant status |
| **invite** | [`flags.2?ExportedChatInvite`](type/ExportedChatInvite) | Chat invite used to join the channel/supergroup |
| <mark>qts</mark> | [`int`](type/int) | New qts value, see updates » for more info |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateChannelParticipant(
	via_chatlist : true,
	channel_id : -828492194464319397,
	date : 97,
	actor_id : 2490463940942528439,
	user_id : -8206449761825546220,
	prev_participant : $client->channelParticipant(
		user_id : -531877911269149627,
		date : 37,
		subscription_until_date : 87,
	),
	new_participant : $client->channelParticipant(
		user_id : -3142978583846074280,
		date : 8,
		subscription_until_date : 75,
	),
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'sz9024cyvCq7V83L',
		admin_id : 4888929303725552237,
		date : 10,
		start_date : 80,
		expire_date : 88,
		usage_limit : 76,
		usage : 36,
		requested : 48,
		subscription_expired : 2,
		title : '5xdZBa1fcu7g0oCh',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 51,
			amount : -8092855633221441937,
		),
	),
	qts : 89,
);
```