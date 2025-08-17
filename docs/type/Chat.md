# Chat

**Description** : *Object defines a group*

**Layer** : 211

```tl
chatEmpty#29562865 id:long = Chat;
chat#41cbf256 flags:# creator:flags.0?true left:flags.2?true deactivated:flags.5?true call_active:flags.23?true call_not_empty:flags.24?true noforwards:flags.25?true id:long title:string photo:ChatPhoto participants_count:int date:int version:int migrated_to:flags.6?InputChannel admin_rights:flags.14?ChatAdminRights default_banned_rights:flags.18?ChatBannedRights = Chat;
chatForbidden#6592a1a7 id:long title:string = Chat;
channel#fe685355 flags:# creator:flags.0?true left:flags.2?true broadcast:flags.5?true verified:flags.7?true megagroup:flags.8?true restricted:flags.9?true signatures:flags.11?true min:flags.12?true scam:flags.19?true has_link:flags.20?true has_geo:flags.21?true slowmode_enabled:flags.22?true call_active:flags.23?true call_not_empty:flags.24?true fake:flags.25?true gigagroup:flags.26?true noforwards:flags.27?true join_to_send:flags.28?true join_request:flags.29?true forum:flags.30?true flags2:# stories_hidden:flags2.1?true stories_hidden_min:flags2.2?true stories_unavailable:flags2.3?true signature_profiles:flags2.12?true autotranslation:flags2.15?true broadcast_messages_allowed:flags2.16?true monoforum:flags2.17?true forum_tabs:flags2.19?true id:long access_hash:flags.13?long title:string username:flags.6?string photo:ChatPhoto date:int restriction_reason:flags.9?Vector<RestrictionReason> admin_rights:flags.14?ChatAdminRights banned_rights:flags.15?ChatBannedRights default_banned_rights:flags.18?ChatBannedRights participants_count:flags.17?int usernames:flags2.0?Vector<Username> stories_max_id:flags2.4?int color:flags2.7?PeerColor profile_color:flags2.8?PeerColor emoji_status:flags2.9?EmojiStatus level:flags2.10?int subscription_until_date:flags2.11?int bot_verification_icon:flags2.13?long send_paid_messages_stars:flags2.14?long linked_monoforum_id:flags2.18?long = Chat;
channelForbidden#17d493d5 flags:# broadcast:flags.5?true megagroup:flags.8?true id:long access_hash:long title:string until_date:flags.16?int = Chat;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**chatEmpty**](constructor/chatEmpty) | Empty constructor, group doesn't exist |
| [**chat**](constructor/chat) | Info about a group.When updating the local peer database, all fields from the newly received constructor take priority over the old constructor cached locally (including by removing fields that aren't set in the new constructor).See here » for an implementation of the logic to use when updating the local user peer database |
| [**chatForbidden**](constructor/chatForbidden) | A group to which the user has no access. E.g., because the user was kicked from the group |
| [**channel**](constructor/channel) | Channel/supergroup infoWhen updating the local peer database, all fields from the newly received constructor take priority over the old constructor cached locally (including by removing fields that aren't set in the new constructor).The only exception to the above rule is when the min flag is set, in which case only the following fields must be applied over any locally stored version:- title- megagroup- color- photo- username- usernames- has_geo- noforwards- emoji_status- has_link- slow_mode_enabled- scam- fake- gigagroup- forum- level- restricted- restriction_reason- join_to_send- join_request- is_verified- default_banned_rights- signature_profilesSee here » for an implementation of the logic to use when updating the local user peer database |
| [**channelForbidden**](constructor/channelForbidden) | Indicates a channel/supergroup we can't access because we were banned, or for some other reason |