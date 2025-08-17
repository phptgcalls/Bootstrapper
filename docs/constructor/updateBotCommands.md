# updateBotCommands

**Description** : *The command set of a certain bot in a certain chat has changed*

**Layer** : 211

```tl
updateBotCommands#4d712f2e peer:Peer bot_id:long commands:Vector<BotCommand> = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`Peer`](type/Peer) | The affected chat |
| <mark>bot_id</mark> | [`long`](type/long) | ID of the bot that changed its command set |
| <mark>commands</mark> | [`Vector<BotCommand>`](type/BotCommand) | New bot commands |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotCommands(
	peer : $client->peerUser(
		user_id : 3177364293895120668,
	),
	bot_id : -6344129622339389633,
	commands : array(
		$client->botCommand(
			command : '851xMBqWVU0IbRck',
			description : 'rNS8HCRml07BiXn3',
		),
	),
);
```