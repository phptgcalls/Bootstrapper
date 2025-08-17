# bots.resetBotCommands

**Description** : *Clear bot commands for the specified bot scope and language code*

**Layer** : 211

```tl
bots.resetBotCommands#3d8de0f9 scope:BotCommandScope lang_code:string = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>scope</mark> | [`BotCommandScope`](type/BotCommandScope) | Command scope |
| <mark>lang_code</mark> | [`string`](type/string) | Language code |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **LANG_CODE_INVALID** | `400` | The specified language code is invalid |
| **USER_BOT_REQUIRED** | `400` | This method can only be called by a bot |

---

## Example

```php
$bool = $client->bots->resetBotCommands(
	scope : $client->botCommandScopeDefault(),
	lang_code : 'Gu8EDxof7IRW5Nt3',
);
```