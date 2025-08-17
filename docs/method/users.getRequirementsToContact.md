# users.getRequirementsToContact

**Layer** : 211

```tl
users.getRequirementsToContact#d89a83a3 id:Vector<InputUser> = Vector<RequirementToContact>;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`Vector<InputUser>`](type/InputUser) | NOTHING |

---

## Result

[Vector<RequirementToContact>](type/RequirementToContact)

---

## Example

```php
$requirementToContact = $client->users->getRequirementsToContact(
	id : array(
		$client->inputUserEmpty(),
		$client->inputUserSelf(),
		$client->inputUser(
			user_id : -6840795957004290242,
			access_hash : -7989506398390218561,
		),
		$client->inputUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 93,
			user_id : -2339287172828979733,
		),
	),
);
```