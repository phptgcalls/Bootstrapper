# messages.setBotPrecheckoutResults

**Description** : *Once the user has confirmed their payment and shipping details, the bot receives an updateBotPrecheckoutQuery update.
Use this method to respond to such pre-checkout queries.
Note: Telegram must receive an answer within 10 seconds after the pre-checkout query was sent*

**Layer** : 211

```tl
messages.setBotPrecheckoutResults#9c2dd95 flags:# success:flags.1?true query_id:long error:flags.0?string = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **success** | [`flags.1?true`](type/true) | Set this flag if everything is alright (goods are available, etc.) and the bot is ready to proceed with the order, otherwise do not set it, and set the error field, instead |
| <mark>query_id</mark> | [`long`](type/long) | Unique identifier for the query to be answered |
| **error** | [`flags.0?string`](type/string) | Required if the success isn't set. Error message in human readable form that explains the reason for failure to proceed with the checkout (e.g. "Sorry, somebody just bought the last of our amazing black T-shirts while you were busy filling out your payment details. Please choose a different color or garment!"). Telegram will display this message to the user |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **ERROR_TEXT_EMPTY** | `400` | The provided error message is empty |
| **USER_BOT_REQUIRED** | `400` | This method can only be called by a bot |

---

## Example

```php
$bool = $client->messages->setBotPrecheckoutResults(
	success : true,
	query_id : -4901796721407290122,
	error : 'EqAwSoXL9JduxPnY',
);
```