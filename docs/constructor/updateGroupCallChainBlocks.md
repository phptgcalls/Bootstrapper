# updateGroupCallChainBlocks

**Layer** : 211

```tl
updateGroupCallChainBlocks#a477288f call:InputGroupCall sub_chain_id:int blocks:Vector<bytes> next_offset:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>call</mark> | [`InputGroupCall`](type/InputGroupCall) | NOTHING |
| <mark>sub_chain_id</mark> | [`int`](type/int) | NOTHING |
| <mark>blocks</mark> | [`Vector<bytes>`](type/bytes) | NOTHING |
| <mark>next_offset</mark> | [`int`](type/int) | NOTHING |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateGroupCallChainBlocks(
	call : $client->inputGroupCall(
		id : 4694939302414694639,
		access_hash : 1301878969507660692,
	),
	sub_chain_id : 74,
	blocks : array('0p?z?LiveProto]H\\?Q'),
	next_offset : 28,
);
```