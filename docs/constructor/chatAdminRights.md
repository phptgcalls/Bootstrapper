# chatAdminRights

**Description** : *Represents the rights of an admin in a channel/supergroup*

**Layer** : 211

```tl
chatAdminRights#5fb224d5 flags:# change_info:flags.0?true post_messages:flags.1?true edit_messages:flags.2?true delete_messages:flags.3?true ban_users:flags.4?true invite_users:flags.5?true pin_messages:flags.7?true add_admins:flags.9?true anonymous:flags.10?true manage_call:flags.11?true other:flags.12?true manage_topics:flags.13?true post_stories:flags.14?true edit_stories:flags.15?true delete_stories:flags.16?true manage_direct_messages:flags.17?true = ChatAdminRights;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **change_info** | [`flags.0?true`](type/true) | If set, allows the admin to modify the description of the channel/supergroup |
| **post_messages** | [`flags.1?true`](type/true) | If set, allows the admin to post messages in the channel |
| **edit_messages** | [`flags.2?true`](type/true) | If set, allows the admin to also edit messages from other admins in the channel |
| **delete_messages** | [`flags.3?true`](type/true) | If set, allows the admin to also delete messages from other admins in the channel |
| **ban_users** | [`flags.4?true`](type/true) | If set, allows the admin to ban users from the channel/supergroup |
| **invite_users** | [`flags.5?true`](type/true) | If set, allows the admin to invite users in the channel/supergroup |
| **pin_messages** | [`flags.7?true`](type/true) | If set, allows the admin to pin messages in the channel/supergroup |
| **add_admins** | [`flags.9?true`](type/true) | If set, allows the admin to add other admins with the same (or more limited) permissions in the channel/supergroup |
| **anonymous** | [`flags.10?true`](type/true) | Whether this admin is anonymous |
| **manage_call** | [`flags.11?true`](type/true) | If set, allows the admin to change group call/livestream settings |
| **other** | [`flags.12?true`](type/true) | Set this flag if none of the other flags are set, but you still want the user to be an admin: if this or any of the other flags are set, the admin can get the chat admin log, get chat statistics, get message statistics in channels, get channel members, see anonymous administrators in supergroups and ignore slow mode |
| **manage_topics** | [`flags.13?true`](type/true) | If set, allows the admin to create, delete or modify forum topics » |
| **post_stories** | [`flags.14?true`](type/true) | If set, allows the admin to post stories as the channel |
| **edit_stories** | [`flags.15?true`](type/true) | If set, allows the admin to edit stories posted by the other admins of the channel |
| **delete_stories** | [`flags.16?true`](type/true) | If set, allows the admin to delete stories posted by the other admins of the channel |
| **manage_direct_messages** | [`flags.17?true`](type/true) | NOTHING |

---

## Type

[ChatAdminRights](type/ChatAdminRights)

---

## Example

```php
$chatAdminRights = $client->chatAdminRights(
	change_info : true,
	post_messages : true,
	edit_messages : true,
	delete_messages : true,
	ban_users : true,
	invite_users : true,
	pin_messages : true,
	add_admins : true,
	anonymous : true,
	manage_call : true,
	other : true,
	manage_topics : true,
	post_stories : true,
	edit_stories : true,
	delete_stories : true,
	manage_direct_messages : true,
);
```