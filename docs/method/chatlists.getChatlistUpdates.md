# chatlists.getChatlistUpdates

**Description** : *Fetch new chats associated with an imported chat folder deep link ». Must be invoked at most every chatlist_update_period seconds (as per the related client configuration parameter »)*

**Layer** : 211

```tl
chatlists.getChatlistUpdates#89419521 chatlist:InputChatlist = chatlists.ChatlistUpdates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chatlist</mark> | [`InputChatlist`](type/InputChatlist) | The folder |

---

## Result

[chatlists.ChatlistUpdates](type/chatlists.ChatlistUpdates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **FILTER_ID_INVALID** | `400` | The specified filter ID is invalid |
| **FILTER_NOT_SUPPORTED** | `400` | The specified filter cannot be used in this context |
| **INPUT_CHATLIST_INVALID** | `400` | The specified folder is invalid |

---

## Example

```php
$chatlistsChatlistUpdates = $client->chatlists->getChatlistUpdates(
	chatlist : $client->inputChatlistDialogFilter(
		filter_id : 44,
	),
);
```