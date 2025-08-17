# updateBotBusinessConnect

**Description** : *Connecting or disconnecting a business bot or changing the connection settings will emit an updateBotBusinessConnect update to the bot, with the new settings and a connection_id that will be used by the bot to handle updates from and send messages as the user*

**Layer** : 211

```tl
updateBotBusinessConnect#8ae5c97a connection:BotBusinessConnection qts:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>connection</mark> | [`BotBusinessConnection`](type/BotBusinessConnection) | Business connection settings |
| <mark>qts</mark> | [`int`](type/int) | New qts value, see updates » for more info |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotBusinessConnect(
	connection : $client->botBusinessConnection(
		disabled : true,
		connection_id : 'eFZEIwpAWVc8BCzK',
		user_id : 379295219262822176,
		dc_id : 2,
		date : 20,
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
	),
	qts : 50,
);
```