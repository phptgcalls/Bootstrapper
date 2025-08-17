# phone.getGroupCallChainBlocks

**Layer** : 211

```tl
phone.getGroupCallChainBlocks#ee9f88a6 call:InputGroupCall sub_chain_id:int offset:int limit:int = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>call</mark> | [`InputGroupCall`](type/InputGroupCall) | NOTHING |
| <mark>sub_chain_id</mark> | [`int`](type/int) | NOTHING |
| <mark>offset</mark> | [`int`](type/int) | NOTHING |
| <mark>limit</mark> | [`int`](type/int) | NOTHING |

---

## Result

[Updates](type/Updates)

---

## Example

```php
$updates = $client->phone->getGroupCallChainBlocks(
	call : $client->inputGroupCall(
		id : 4920998949441669355,
		access_hash : -5239325767761953892,
	),
	sub_chain_id : 68,
	offset : 100,
	limit : 75,
);
```