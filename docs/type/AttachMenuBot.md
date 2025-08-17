# AttachMenuBot

**Description** : *Represents a bot mini app that can be launched from the attachment menu »*

**Layer** : 211

```tl
attachMenuBot#d90d8dfe flags:# inactive:flags.0?true has_settings:flags.1?true request_write_access:flags.2?true show_in_attach_menu:flags.3?true show_in_side_menu:flags.4?true side_menu_disclaimer_needed:flags.5?true bot_id:long short_name:string peer_types:flags.3?Vector<AttachMenuPeerType> icons:Vector<AttachMenuBotIcon> = AttachMenuBot;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**attachMenuBot**](constructor/attachMenuBot) | Represents a bot mini app that can be launched from the attachment/side menu »At least one of the show_in_attach_menu or the show_in_side_menu flags will always be set |