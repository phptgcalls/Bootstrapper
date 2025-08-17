# messageActionSuggestedPostApproval

**Layer** : 211

```tl
messageActionSuggestedPostApproval#ee7a1596 flags:# rejected:flags.0?true balance_too_low:flags.1?true reject_comment:flags.2?string schedule_date:flags.3?int price:flags.4?StarsAmount = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **rejected** | [`flags.0?true`](type/true) | NOTHING |
| **balance_too_low** | [`flags.1?true`](type/true) | NOTHING |
| **reject_comment** | [`flags.2?string`](type/string) | NOTHING |
| **schedule_date** | [`flags.3?int`](type/int) | NOTHING |
| **price** | [`flags.4?StarsAmount`](type/StarsAmount) | NOTHING |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionSuggestedPostApproval(
	rejected : true,
	balance_too_low : true,
	reject_comment : 'AtGefqQHZDFwvgCk',
	schedule_date : 94,
	price : $client->starsAmount(
		amount : 6958751783271111103,
		nanos : 64,
	),
);
```