# sendMessageEmojiInteractionSeen

**Description** : *User is watching an animated emoji reaction triggered by another user, click here for more info »*

**Layer** : 211

```tl
sendMessageEmojiInteractionSeen#b665902e emoticon:string = SendMessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>emoticon</mark> | [`string`](type/string) | Emoji |

---

## Type

[SendMessageAction](type/SendMessageAction)

---

## Example

```php
$sendMessageAction = $client->sendMessageEmojiInteractionSeen(
	emoticon : 'g3XzfrPQaY1lyGB8',
);
```