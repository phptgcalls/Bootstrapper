# connectedBot

**Description** : *Contains info about a connected business bot »*

**Layer** : 211

```tl
connectedBot#cd64636c flags:# bot_id:long recipients:BusinessBotRecipients rights:BusinessBotRights = ConnectedBot;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>bot_id</mark> | [`long`](type/long) | ID of the connected bot |
| <mark>recipients</mark> | [`BusinessBotRecipients`](type/BusinessBotRecipients) | Specifies the private chats that a connected business bot » may receive messages and interact with |
| <mark>rights</mark> | [`BusinessBotRights`](type/BusinessBotRights) | NOTHING |

---

## Type

[ConnectedBot](type/ConnectedBot)

---

## Example

```php
$connectedBot = $client->connectedBot(
	bot_id : 8906310671199663077,
	recipients : $client->businessBotRecipients(
		existing_chats : true,
		new_chats : true,
		contacts : true,
		non_contacts : true,
		exclude_selected : true,
		users : array(-1233496605286282797),
		exclude_users : array(-2389865803186300208),
	),
	rights : $client->businessBotRights(
		reply : true,
		read_messages : true,
		delete_sent_messages : true,
		delete_received_messages : true,
		edit_name : true,
		edit_bio : true,
		edit_profile_photo : true,
		edit_username : true,
		view_gifts : true,
		sell_gifts : true,
		change_gift_settings : true,
		transfer_and_upgrade_gifts : true,
		transfer_stars : true,
		manage_stories : true,
	),
);
```