# businessRecipients

**Description** : *Specifies the chats that can receive Telegram Business away » and greeting » messages*

**Layer** : 211

```tl
businessRecipients#21108ff7 flags:# existing_chats:flags.0?true new_chats:flags.1?true contacts:flags.2?true non_contacts:flags.3?true exclude_selected:flags.5?true users:flags.4?Vector<long> = BusinessRecipients;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **existing_chats** | [`flags.0?true`](type/true) | All existing private chats |
| **new_chats** | [`flags.1?true`](type/true) | All new private chats |
| **contacts** | [`flags.2?true`](type/true) | All private chats with contacts |
| **non_contacts** | [`flags.3?true`](type/true) | All private chats with non-contacts |
| **exclude_selected** | [`flags.5?true`](type/true) | If set, inverts the selection |
| **users** | [`flags.4?Vector<long>`](type/long) | Only private chats with the specified users |

---

## Type

[BusinessRecipients](type/BusinessRecipients)

---

## Example

```php
$businessRecipients = $client->businessRecipients(
	existing_chats : true,
	new_chats : true,
	contacts : true,
	non_contacts : true,
	exclude_selected : true,
	users : array(7319675654399146690),
);
```