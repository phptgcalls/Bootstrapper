# updateBotChatBoost

**Description** : *A channel/supergroup boost has changed (bots only)*

**Layer** : 211

```tl
updateBotChatBoost#904dd49c peer:Peer boost:Boost qts:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | Channel |
| <mark>boost</mark> | [`Boost`](type/Boost) | New boost information |
| <mark>qts</mark> | [`int`](type/int) | QTS event sequence identifier |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotChatBoost(
	peer : $client->peerUser(
		user_id : -7448790080635338438,
	),
	boost : $client->boost(
		gift : true,
		giveaway : true,
		unclaimed : true,
		id : 'c7we2G4MjfxaZLd5',
		user_id : 5979315158910848640,
		giveaway_msg_id : 34,
		date : 5,
		expires : 56,
		used_gift_slug : 'PRS0rGeB7mJC5l4h',
		multiplier : 19,
		stars : -4690429185527222664,
	),
	qts : 51,
);
```