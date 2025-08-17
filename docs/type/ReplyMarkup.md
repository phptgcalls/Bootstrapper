# ReplyMarkup

**Description** : *Reply markup for bot and inline keyboards*

**Layer** : 211

```tl
replyKeyboardHide#a03e5b85 flags:# selective:flags.2?true = ReplyMarkup;
replyKeyboardForceReply#86b40b08 flags:# single_use:flags.1?true selective:flags.2?true placeholder:flags.3?string = ReplyMarkup;
replyKeyboardMarkup#85dd99d1 flags:# resize:flags.0?true single_use:flags.1?true selective:flags.2?true persistent:flags.4?true rows:Vector<KeyboardButtonRow> placeholder:flags.3?string = ReplyMarkup;
replyInlineMarkup#48a30254 rows:Vector<KeyboardButtonRow> = ReplyMarkup;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**replyKeyboardHide**](constructor/replyKeyboardHide) | Hide sent bot keyboard |
| [**replyKeyboardForceReply**](constructor/replyKeyboardForceReply) | Force the user to send a reply |
| [**replyKeyboardMarkup**](constructor/replyKeyboardMarkup) | Bot keyboard |
| [**replyInlineMarkup**](constructor/replyInlineMarkup) | Bot or inline keyboard |