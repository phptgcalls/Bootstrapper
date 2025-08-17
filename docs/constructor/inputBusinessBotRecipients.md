# inputBusinessBotRecipients

**Description** : *Specifies the private chats that a connected business bot » may interact with*

**Layer** : 211

```tl
inputBusinessBotRecipients#c4e5921e flags:# existing_chats:flags.0?true new_chats:flags.1?true contacts:flags.2?true non_contacts:flags.3?true exclude_selected:flags.5?true users:flags.4?Vector<InputUser> exclude_users:flags.6?Vector<InputUser> = InputBusinessBotRecipients;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **existing_chats** | [`flags.0?true`](type/true) | Selects all existing private chats |
| **new_chats** | [`flags.1?true`](type/true) | Selects all new private chats |
| **contacts** | [`flags.2?true`](type/true) | Selects all private chats with contacts |
| **non_contacts** | [`flags.3?true`](type/true) | Selects all private chats with non-contacts |
| **exclude_selected** | [`flags.5?true`](type/true) | If set, then all private chats except the ones selected by existing_chats, new_chats, contacts, non_contacts and users are chosen. Note that if this flag is set, any values passed in exclude_users will be merged and moved into users by the server |
| **users** | [`flags.4?Vector<InputUser>`](type/InputUser) | Explicitly selected private chats |
| **exclude_users** | [`flags.6?Vector<InputUser>`](type/InputUser) | Identifiers of private chats that are always excluded |

---

## Type

[InputBusinessBotRecipients](type/InputBusinessBotRecipients)

---

## Example

```php
$inputBusinessBotRecipients = $client->inputBusinessBotRecipients(
	existing_chats : true,
	new_chats : true,
	contacts : true,
	non_contacts : true,
	exclude_selected : true,
	users : array(
		$client->inputUserEmpty(),
		$client->inputUserSelf(),
		$client->inputUser(
			user_id : 848830742714866512,
			access_hash : 4766530396845472231,
		),
		$client->inputUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 20,
			user_id : -3034406210792520447,
		),
	),
	exclude_users : array(
		$client->inputUserEmpty(),
		$client->inputUserSelf(),
		$client->inputUser(
			user_id : 4126618822880748328,
			access_hash : 7340823053915509457,
		),
		$client->inputUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 22,
			user_id : -8418984480005289802,
		),
	),
);
```