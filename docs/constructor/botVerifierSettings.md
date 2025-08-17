# botVerifierSettings

**Layer** : 211

```tl
botVerifierSettings#b0cd6617 flags:# can_modify_custom_description:flags.1?true icon:long company:string custom_description:flags.0?string = BotVerifierSettings;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | NOTHING |
| **can_modify_custom_description** | [`flags.1?true`](type/true) | NOTHING |
| <mark>icon</mark> | [`long`](type/long) | NOTHING |
| <mark>company</mark> | [`string`](type/string) | NOTHING |
| **custom_description** | [`flags.0?string`](type/string) | NOTHING |

---

## Type

[BotVerifierSettings](type/BotVerifierSettings)

---

## Example

```php
$botVerifierSettings = $client->botVerifierSettings(
	can_modify_custom_description : true,
	icon : -4796469818815023722,
	company : 'IkpqsEPCKVNdn2vZ',
	custom_description : '9JTI7yKftPHBXd1h',
);
```