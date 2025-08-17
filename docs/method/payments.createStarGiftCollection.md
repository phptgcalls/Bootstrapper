# payments.createStarGiftCollection

**Layer** : 211

```tl
payments.createStarGiftCollection#1f4a0e87 peer:InputPeer title:string stargift:Vector<InputSavedStarGift> = StarGiftCollection;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | NOTHING |
| <mark>title</mark> | [`string`](type/string) | NOTHING |
| <mark>stargift</mark> | [`Vector<InputSavedStarGift>`](type/InputSavedStarGift) | NOTHING |

---

## Result

[StarGiftCollection](type/StarGiftCollection)

---

## Example

```php
$starGiftCollection = $client->payments->createStarGiftCollection(
	peer : $client->inputPeerEmpty(),
	title : 'uYqGCbMl4OW6NPpZ',
	stargift : array(
		$client->inputSavedStarGiftUser(
			msg_id : 48,
		),
		$client->inputSavedStarGiftChat(
			peer : $client->inputPeerEmpty(),
			saved_id : 590162480398922380,
		),
		$client->inputSavedStarGiftSlug(
			slug : 'iYP3FvSK7efoADt8',
		),
	),
);
```