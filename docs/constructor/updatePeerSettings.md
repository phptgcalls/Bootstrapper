# updatePeerSettings

**Description** : *Settings of a certain peer have changed*

**Layer** : 211

```tl
updatePeerSettings#6a7e7366 peer:Peer settings:PeerSettings = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | The peer |
| <mark>settings</mark> | [`PeerSettings`](type/PeerSettings) | Associated peer settings |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updatePeerSettings(
	peer : $client->peerUser(
		user_id : 1359982579609605173,
	),
	settings : $client->peerSettings(
		report_spam : true,
		add_contact : true,
		block_contact : true,
		share_contact : true,
		need_contacts_exception : true,
		report_geo : true,
		autoarchived : true,
		invite_members : true,
		request_chat_broadcast : true,
		business_bot_paused : true,
		business_bot_can_reply : true,
		geo_distance : 5,
		request_chat_title : '7OJtHPGEzZbM6UQa',
		request_chat_date : 41,
		business_bot_id : -4402626088141991825,
		business_bot_manage_url : 'https://docs.liveproto.dev',
		charge_paid_message_stars : 2325578575444470542,
		registration_month : 'PKSictk8LEf50haI',
		phone_country : '+1234567890',
		name_change_date : 13,
		photo_change_date : 57,
	),
);
```