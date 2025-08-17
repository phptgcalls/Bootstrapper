# botCommand

**Description** : *Describes a bot command that can be used in a chat*

**Layer** : 211

```tl
botCommand#c27ac8c7 command:string description:string = BotCommand;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>command</mark> | [`string`](type/string) | /command name |
| <mark>description</mark> | [`string`](type/string) | Description of the command |

---

## Type

[BotCommand](type/BotCommand)

---

## Example

```php
$botCommand = $client->botCommand(
	command : 'tOak3gqFolsvZGWb',
	description : '8MTZQbw9JmRBjv7i',
);
```