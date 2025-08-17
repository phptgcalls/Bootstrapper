# inputEncryptedChat

**Description** : *Creates an encrypted chat*

**Layer** : 211

```tl
inputEncryptedChat#f141b5e1 chat_id:int access_hash:long = InputEncryptedChat;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chat_id</mark> | [`int`](type/int) | Chat ID |
| <mark>access_hash</mark> | [`long`](type/long) | Checking sum from constructor encryptedChat, encryptedChatWaiting or encryptedChatRequested |

---

## Type

[InputEncryptedChat](type/InputEncryptedChat)

---

## Example

```php
$inputEncryptedChat = $client->inputEncryptedChat(
	chat_id : 17,
	access_hash : -4259960921908992270,
);
```