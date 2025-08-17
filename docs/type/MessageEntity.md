# MessageEntity

**Description** : *Message entities, representing styled text in a message*

**Layer** : 211

```tl
messageEntityUnknown#bb92ba95 offset:int length:int = MessageEntity;
messageEntityMention#fa04579d offset:int length:int = MessageEntity;
messageEntityHashtag#6f635b0d offset:int length:int = MessageEntity;
messageEntityBotCommand#6cef8ac7 offset:int length:int = MessageEntity;
messageEntityUrl#6ed02538 offset:int length:int = MessageEntity;
messageEntityEmail#64e475c2 offset:int length:int = MessageEntity;
messageEntityBold#bd610bc9 offset:int length:int = MessageEntity;
messageEntityItalic#826f8b60 offset:int length:int = MessageEntity;
messageEntityCode#28a20571 offset:int length:int = MessageEntity;
messageEntityPre#73924be0 offset:int length:int language:string = MessageEntity;
messageEntityTextUrl#76a6d327 offset:int length:int url:string = MessageEntity;
messageEntityMentionName#dc7b1140 offset:int length:int user_id:long = MessageEntity;
inputMessageEntityMentionName#208e68c9 offset:int length:int user_id:InputUser = MessageEntity;
messageEntityPhone#9b69e34b offset:int length:int = MessageEntity;
messageEntityCashtag#4c4e743f offset:int length:int = MessageEntity;
messageEntityUnderline#9c4e7e8b offset:int length:int = MessageEntity;
messageEntityStrike#bf0693d4 offset:int length:int = MessageEntity;
messageEntityBankCard#761e6af4 offset:int length:int = MessageEntity;
messageEntitySpoiler#32ca960f offset:int length:int = MessageEntity;
messageEntityCustomEmoji#c8cf05f8 offset:int length:int document_id:long = MessageEntity;
messageEntityBlockquote#f1ccaaac flags:# collapsed:flags.0?true offset:int length:int = MessageEntity;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**messageEntityUnknown**](constructor/messageEntityUnknown) | Unknown message entity |
| [**messageEntityMention**](constructor/messageEntityMention) | Message entity mentioning a user by @username; messageEntityMentionName can also be used to mention users by their ID |
| [**messageEntityHashtag**](constructor/messageEntityHashtag) | #hashtag message entity |
| [**messageEntityBotCommand**](constructor/messageEntityBotCommand) | Message entity representing a bot /command |
| [**messageEntityUrl**](constructor/messageEntityUrl) | Message entity representing an in-text url: https://google.com; for text urls, use messageEntityTextUrl |
| [**messageEntityEmail**](constructor/messageEntityEmail) | Message entity representing an email@example.com |
| [**messageEntityBold**](constructor/messageEntityBold) | Message entity representing bold text |
| [**messageEntityItalic**](constructor/messageEntityItalic) | Message entity representing italic text |
| [**messageEntityCode**](constructor/messageEntityCode) | Message entity representing a codeblock |
| [**messageEntityPre**](constructor/messageEntityPre) | Message entity representing a preformatted codeblock, allowing the user to specify a programming language for the codeblock |
| [**messageEntityTextUrl**](constructor/messageEntityTextUrl) | Message entity representing a text url: for in-text urls like https://google.com use messageEntityUrl.Note that an additional confirmation popup with the full URL must be displayed to the user before opening this link, unless the domain satisfies the conditions specified in the domain whitelist documentation » |
| [**messageEntityMentionName**](constructor/messageEntityMentionName) | Message entity representing a user mention: for creating a mention use inputMessageEntityMentionName |
| [**inputMessageEntityMentionName**](constructor/inputMessageEntityMentionName) | Message entity that can be used to create a user user mention: received mentions use the messageEntityMentionName constructor, instead |
| [**messageEntityPhone**](constructor/messageEntityPhone) | Message entity representing a phone number |
| [**messageEntityCashtag**](constructor/messageEntityCashtag) | Message entity representing a $cashtag |
| [**messageEntityUnderline**](constructor/messageEntityUnderline) | Message entity representing underlined text |
| [**messageEntityStrike**](constructor/messageEntityStrike) | Message entity representing strikethrough text |
| [**messageEntityBankCard**](constructor/messageEntityBankCard) | Indicates a credit card number |
| [**messageEntitySpoiler**](constructor/messageEntitySpoiler) | Message entity representing a spoiler |
| [**messageEntityCustomEmoji**](constructor/messageEntityCustomEmoji) | Represents a custom emoji.  Note that this entity must wrap exactly one regular emoji (the one contained in documentAttributeCustomEmoji.alt) in the related text, otherwise the server will ignore it |
| [**messageEntityBlockquote**](constructor/messageEntityBlockquote) | Message entity representing a block quote |