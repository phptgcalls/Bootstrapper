# PrivacyRule

**Description** : *Privacy rules together with privacy keys indicate what can or can't someone do and are specified by a PrivacyRule constructor, and its input counterpart InputPrivacyRule*

**Layer** : 211

```tl
privacyValueAllowContacts#fffe1bac = PrivacyRule;
privacyValueAllowAll#65427b82 = PrivacyRule;
privacyValueAllowUsers#b8905fb2 users:Vector<long> = PrivacyRule;
privacyValueDisallowContacts#f888fa1a = PrivacyRule;
privacyValueDisallowAll#8b73e763 = PrivacyRule;
privacyValueDisallowUsers#e4621141 users:Vector<long> = PrivacyRule;
privacyValueAllowChatParticipants#6b134e8e chats:Vector<long> = PrivacyRule;
privacyValueDisallowChatParticipants#41c87565 chats:Vector<long> = PrivacyRule;
privacyValueAllowCloseFriends#f7e8d89b = PrivacyRule;
privacyValueAllowPremium#ece9814b = PrivacyRule;
privacyValueAllowBots#21461b5d = PrivacyRule;
privacyValueDisallowBots#f6a5f82f = PrivacyRule;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**privacyValueAllowContacts**](constructor/privacyValueAllowContacts) | Allow all contacts |
| [**privacyValueAllowAll**](constructor/privacyValueAllowAll) | Allow all users |
| [**privacyValueAllowUsers**](constructor/privacyValueAllowUsers) | Allow only certain users |
| [**privacyValueDisallowContacts**](constructor/privacyValueDisallowContacts) | Disallow only contacts |
| [**privacyValueDisallowAll**](constructor/privacyValueDisallowAll) | Disallow all users |
| [**privacyValueDisallowUsers**](constructor/privacyValueDisallowUsers) | Disallow only certain users |
| [**privacyValueAllowChatParticipants**](constructor/privacyValueAllowChatParticipants) | Allow all participants of certain chats |
| [**privacyValueDisallowChatParticipants**](constructor/privacyValueDisallowChatParticipants) | Disallow only participants of certain chats |
| [**privacyValueAllowCloseFriends**](constructor/privacyValueAllowCloseFriends) | Allow only close friends » |
| [**privacyValueAllowPremium**](constructor/privacyValueAllowPremium) | Allow only users with a Premium subscription », currently only usable for inputPrivacyKeyChatInvite |
| [**privacyValueAllowBots**](constructor/privacyValueAllowBots) | Allow bots and mini apps |
| [**privacyValueDisallowBots**](constructor/privacyValueDisallowBots) | Disallow bots and mini apps |