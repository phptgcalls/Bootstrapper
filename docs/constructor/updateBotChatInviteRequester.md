# updateBotChatInviteRequester

**Description** : *Someone has requested to join a chat or channel (bots only, users will receive an updatePendingJoinRequests, instead)*

**Layer** : 211

```tl
updateBotChatInviteRequester#11dfa986 peer:Peer date:int user_id:long about:string invite:ExportedChatInvite qts:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | The chat or channel in question |
| <mark>date</mark> | [`int`](type/int) | When was the join request » made |
| <mark>user_id</mark> | [`long`](type/long) | The user ID that is asking to join the chat or channel |
| <mark>about</mark> | [`string`](type/string) | Bio of the user |
| <mark>invite</mark> | [`ExportedChatInvite`](type/ExportedChatInvite) | Chat invite link that was used by the user to send the join request » |
| <mark>qts</mark> | [`int`](type/int) | QTS event sequence identifier |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotChatInviteRequester(
	peer : $client->peerUser(
		user_id : 6159507408930961749,
	),
	date : 7,
	user_id : -908876554715436544,
	about : 'H4ybiPKn0uFNW36v',
	invite : $client->chatInviteExported(
		revoked : true,
		permanent : true,
		request_needed : true,
		link : 'sZ4gz0ISX1tLp6lr',
		admin_id : -8518035592193638859,
		date : 33,
		start_date : 84,
		expire_date : 24,
		usage_limit : 1,
		usage : 87,
		requested : 86,
		subscription_expired : 37,
		title : '7uKWUEtM9QBDsezl',
		subscription_pricing : $client->starsSubscriptionPricing(
			period : 65,
			amount : -8733869145607544927,
		),
	),
	qts : 100,
);
```