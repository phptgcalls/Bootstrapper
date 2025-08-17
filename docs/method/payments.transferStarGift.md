# payments.transferStarGift

**Layer** : 211

```tl
payments.transferStarGift#7f18176a stargift:InputSavedStarGift to_id:InputPeer = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>stargift</mark> | [`InputSavedStarGift`](type/InputSavedStarGift) | NOTHING |
| <mark>to_id</mark> | [`InputPeer`](type/InputPeer) | NOTHING |

---

## Result

[Updates](type/Updates)

---

## Example

```php
$updates = $client->payments->transferStarGift(
	stargift : $client->inputSavedStarGiftUser(
		msg_id : 34,
	),
	to_id : $client->inputPeerEmpty(),
);
```