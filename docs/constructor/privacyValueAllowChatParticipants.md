# privacyValueAllowChatParticipants

**Description** : *Allow all participants of certain chats*

**Layer** : 211

```tl
privacyValueAllowChatParticipants#6b134e8e chats:Vector<long> = PrivacyRule;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>chats</mark> | [`Vector<long>`](type/long) | Allowed chats |

---

## Type

[PrivacyRule](type/PrivacyRule)

---

## Example

```php
$privacyRule = $client->privacyValueAllowChatParticipants(
	chats : array(-135459372192003754),
);
```