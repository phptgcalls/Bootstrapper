# BotCommandScope

**Description** : *Represents a scope where the bot commands, specified using bots.setBotCommands will be valid*

**Layer** : 211

```tl
botCommandScopeDefault#2f6cb2ab = BotCommandScope;
botCommandScopeUsers#3c4f04d8 = BotCommandScope;
botCommandScopeChats#6fe1a881 = BotCommandScope;
botCommandScopeChatAdmins#b9aa606a = BotCommandScope;
botCommandScopePeer#db9d897d peer:InputPeer = BotCommandScope;
botCommandScopePeerAdmins#3fd863d1 peer:InputPeer = BotCommandScope;
botCommandScopePeerUser#a1321f3 peer:InputPeer user_id:InputUser = BotCommandScope;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**botCommandScopeDefault**](constructor/botCommandScopeDefault) | The commands will be valid in all dialogs |
| [**botCommandScopeUsers**](constructor/botCommandScopeUsers) | The specified bot commands will only be valid in all private chats with users |
| [**botCommandScopeChats**](constructor/botCommandScopeChats) | The specified bot commands will be valid in all groups and supergroups |
| [**botCommandScopeChatAdmins**](constructor/botCommandScopeChatAdmins) | The specified bot commands will be valid only for chat administrators, in all groups and supergroups |
| [**botCommandScopePeer**](constructor/botCommandScopePeer) | The specified bot commands will be valid only in a specific dialog |
| [**botCommandScopePeerAdmins**](constructor/botCommandScopePeerAdmins) | The specified bot commands will be valid for all admins of the specified group or supergroup |
| [**botCommandScopePeerUser**](constructor/botCommandScopePeerUser) | The specified bot commands will be valid only for a specific user in the specified group or supergroup |