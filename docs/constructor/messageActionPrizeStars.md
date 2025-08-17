# messageActionPrizeStars

**Description** : *You won some Telegram Stars in a Telegram Star giveaway »*

**Layer** : 211

```tl
messageActionPrizeStars#b00c47a2 flags:# unclaimed:flags.0?true stars:long transaction_id:string boost_peer:Peer giveaway_msg_id:int = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **unclaimed** | [`flags.0?true`](type/true) | If set, this indicates the reverse transaction that refunds the remaining stars to the creator of a giveaway if, when the giveaway ends, the number of members in the channel is smaller than the number of winners in the giveaway |
| <mark>stars</mark> | [`long`](type/long) | The number of Telegram Stars you won |
| <mark>transaction_id</mark> | [`string`](type/string) | ID of the telegram star transaction |
| <mark>boost_peer</mark> | [`Peer`](type/Peer) | Identifier of the peer that was automatically boosted by the winners of the giveaway |
| <mark>giveaway_msg_id</mark> | [`int`](type/int) | ID of the message containing the messageMediaGiveaway |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionPrizeStars(
	unclaimed : true,
	stars : -3809534884697122928,
	transaction_id : '1s6v98KGoHQRdpNP',
	boost_peer : $client->peerUser(
		user_id : 3676346808311290618,
	),
	giveaway_msg_id : 46,
);
```