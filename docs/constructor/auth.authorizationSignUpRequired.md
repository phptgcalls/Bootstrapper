# auth.authorizationSignUpRequired

**Description** : *An account with this phone number doesn't exist on telegram: the user has to enter basic information and sign up*

**Layer** : 211

```tl
auth.authorizationSignUpRequired#44747e9a flags:# terms_of_service:flags.0?help.TermsOfService = auth.Authorization;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **terms_of_service** | [`flags.0?help.TermsOfService`](type/help.TermsOfService) | Telegram's terms of service: the user must read and accept the terms of service before signing up to telegram |

---

## Type

[auth.Authorization](type/auth.Authorization)

---

## Example

```php
$authAuthorization = $client->auth->authorizationSignUpRequired(
	terms_of_service : $client->help->termsOfService(
		popup : true,
		id : $client->dataJSON(
			data : 'I45Rp1QAXNkLTaOM',
		),
		text : 'edRT9kuO12hj3JCx',
		entities : array(
			$client->messageEntityUnknown(
				offset : 61,
				length : 85,
			),
			$client->messageEntityMention(
				offset : 51,
				length : 84,
			),
			$client->messageEntityHashtag(
				offset : 74,
				length : 16,
			),
			$client->messageEntityBotCommand(
				offset : 98,
				length : 7,
			),
			$client->messageEntityUrl(
				offset : 13,
				length : 18,
			),
			$client->messageEntityEmail(
				offset : 88,
				length : 56,
			),
			$client->messageEntityBold(
				offset : 85,
				length : 13,
			),
			$client->messageEntityItalic(
				offset : 8,
				length : 76,
			),
			$client->messageEntityCode(
				offset : 99,
				length : 12,
			),
			$client->messageEntityPre(
				offset : 31,
				length : 34,
				language : 'BZGF2vcWrLqMUJpA',
			),
			$client->messageEntityTextUrl(
				offset : 52,
				length : 44,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 70,
				length : 9,
				user_id : 8712937481201111409,
			),
			$client->inputMessageEntityMentionName(
				offset : 7,
				length : 44,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 0,
				length : 85,
			),
			$client->messageEntityCashtag(
				offset : 70,
				length : 40,
			),
			$client->messageEntityUnderline(
				offset : 49,
				length : 0,
			),
			$client->messageEntityStrike(
				offset : 23,
				length : 98,
			),
			$client->messageEntityBankCard(
				offset : 34,
				length : 31,
			),
			$client->messageEntitySpoiler(
				offset : 68,
				length : 94,
			),
			$client->messageEntityCustomEmoji(
				offset : 26,
				length : 81,
				document_id : -3855806064414067580,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 75,
				length : 25,
			),
		),
		min_age_confirm : 43,
	),
);
```