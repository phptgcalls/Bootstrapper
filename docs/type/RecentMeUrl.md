# RecentMeUrl

**Description** : *Recent t.me urls*

**Layer** : 211

```tl
recentMeUrlUnknown#46e1d13d url:string = RecentMeUrl;
recentMeUrlUser#b92c09e2 url:string user_id:long = RecentMeUrl;
recentMeUrlChat#b2da71d2 url:string chat_id:long = RecentMeUrl;
recentMeUrlChatInvite#eb49081d url:string chat_invite:ChatInvite = RecentMeUrl;
recentMeUrlStickerSet#bc0a57dc url:string set:StickerSetCovered = RecentMeUrl;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**recentMeUrlUnknown**](constructor/recentMeUrlUnknown) | Unknown t.me url |
| [**recentMeUrlUser**](constructor/recentMeUrlUser) | Recent t.me link to a user |
| [**recentMeUrlChat**](constructor/recentMeUrlChat) | Recent t.me link to a chat |
| [**recentMeUrlChatInvite**](constructor/recentMeUrlChatInvite) | Recent t.me invite link to a chat |
| [**recentMeUrlStickerSet**](constructor/recentMeUrlStickerSet) | Recent t.me stickerset installation URL |