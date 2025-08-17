# StoryItem

**Description** : *Represents a Telegram Story*

**Layer** : 211

```tl
storyItemDeleted#51e6ee4f id:int = StoryItem;
storyItemSkipped#ffadc913 flags:# close_friends:flags.8?true id:int date:int expire_date:int = StoryItem;
storyItem#edf164f1 flags:# pinned:flags.5?true public:flags.7?true close_friends:flags.8?true min:flags.9?true noforwards:flags.10?true edited:flags.11?true contacts:flags.12?true selected_contacts:flags.13?true out:flags.16?true id:int date:int from_id:flags.18?Peer fwd_from:flags.17?StoryFwdHeader expire_date:int caption:flags.0?string entities:flags.1?Vector<MessageEntity> media:MessageMedia media_areas:flags.14?Vector<MediaArea> privacy:flags.2?Vector<PrivacyRule> views:flags.3?StoryViews sent_reaction:flags.15?Reaction albums:flags.19?Vector<int> = StoryItem;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**storyItemDeleted**](constructor/storyItemDeleted) | Represents a previously active story, that was deleted |
| [**storyItemSkipped**](constructor/storyItemSkipped) | Represents an active story, whose full information was omitted for space and performance reasons; use stories.getStoriesByID to fetch full info about the skipped story when and if needed |
| [**storyItem**](constructor/storyItem) | Represents a story |