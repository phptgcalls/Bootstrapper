# account.setPrivacy

**Description** : *Change privacy settings of current account*

**Layer** : 211

```tl
account.setPrivacy#c9f81ce8 key:InputPrivacyKey rules:Vector<InputPrivacyRule> = account.PrivacyRules;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>key</mark> | [`InputPrivacyKey`](type/InputPrivacyKey) | New privacy rule |
| <mark>rules</mark> | [`Vector<InputPrivacyRule>`](type/InputPrivacyRule) | Peers to which the privacy rule will apply |

---

## Result

[account.PrivacyRules](type/account.PrivacyRules)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **PRIVACY_KEY_INVALID** | `400` | The privacy key is invalid |
| **PRIVACY_TOO_LONG** | `400` | Too many privacy rules were specified, the current limit is 1000 |
| **PRIVACY_VALUE_INVALID** | `400` | The specified privacy rule combination is invalid |

---

## Example

```php
$accountPrivacyRules = $client->account->setPrivacy(
	key : $client->inputPrivacyKeyStatusTimestamp(),
	rules : array(
		$client->inputPrivacyValueAllowContacts(),
		$client->inputPrivacyValueAllowAll(),
		$client->inputPrivacyValueAllowUsers(
			users : array(
				$client->inputUserEmpty(),
				$client->inputUserSelf(),
				$client->inputUser(
					user_id : 5051232955078288303,
					access_hash : 5713051359100436021,
				),
				$client->inputUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 30,
					user_id : 9219087334391956699,
				),
			),
		),
		$client->inputPrivacyValueDisallowContacts(),
		$client->inputPrivacyValueDisallowAll(),
		$client->inputPrivacyValueDisallowUsers(
			users : array(
				$client->inputUserEmpty(),
				$client->inputUserSelf(),
				$client->inputUser(
					user_id : 1683556793022191247,
					access_hash : -525071621417492367,
				),
				$client->inputUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 53,
					user_id : -4293197728057622307,
				),
			),
		),
		$client->inputPrivacyValueAllowChatParticipants(
			chats : array(5750698219372263454),
		),
		$client->inputPrivacyValueDisallowChatParticipants(
			chats : array(7241048700503356989),
		),
		$client->inputPrivacyValueAllowCloseFriends(),
		$client->inputPrivacyValueAllowPremium(),
		$client->inputPrivacyValueAllowBots(),
		$client->inputPrivacyValueDisallowBots(),
	),
);
```