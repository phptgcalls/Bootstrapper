# payments.updateStarGiftCollection

**Layer** : 211

```tl
payments.updateStarGiftCollection#4fddbee7 flags:# peer:InputPeer collection_id:int title:flags.0?string delete_stargift:flags.1?Vector<InputSavedStarGift> add_stargift:flags.2?Vector<InputSavedStarGift> order:flags.3?Vector<InputSavedStarGift> = StarGiftCollection;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | NOTHING |
| <mark>collection_id</mark> | [`int`](type/int) | NOTHING |
| **title** | [`flags.0?string`](type/string) | NOTHING |
| **delete_stargift** | [`flags.1?Vector<InputSavedStarGift>`](type/InputSavedStarGift) | NOTHING |
| **add_stargift** | [`flags.2?Vector<InputSavedStarGift>`](type/InputSavedStarGift) | NOTHING |
| **order** | [`flags.3?Vector<InputSavedStarGift>`](type/InputSavedStarGift) | NOTHING |

---

## Result

[StarGiftCollection](type/StarGiftCollection)

---

## Example

```php
$starGiftCollection = $client->payments->updateStarGiftCollection(
	peer : $client->inputPeerEmpty(),
	collection_id : 75,
	title : 'nvopKf3ZID9BAXFU',
	delete_stargift : array(
		$client->inputSavedStarGiftUser(
			msg_id : 25,
		),
		$client->inputSavedStarGiftChat(
			peer : $client->inputPeerEmpty(),
			saved_id : 4121468052519376526,
		),
		$client->inputSavedStarGiftSlug(
			slug : 'g2546NADqj7vdHGM',
		),
	),
	add_stargift : array(
		$client->inputSavedStarGiftUser(
			msg_id : 78,
		),
		$client->inputSavedStarGiftChat(
			peer : $client->inputPeerEmpty(),
			saved_id : 1057320239568544253,
		),
		$client->inputSavedStarGiftSlug(
			slug : '7DOdVqTlfQFm0Enz',
		),
	),
	order : array(
		$client->inputSavedStarGiftUser(
			msg_id : 19,
		),
		$client->inputSavedStarGiftChat(
			peer : $client->inputPeerEmpty(),
			saved_id : -4855712338666556062,
		),
		$client->inputSavedStarGiftSlug(
			slug : 'yNp9ciHOgePBWxrV',
		),
	),
);
```