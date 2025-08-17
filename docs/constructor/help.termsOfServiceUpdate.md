# help.termsOfServiceUpdate

**Description** : *Info about an update of telegram's terms of service. If the terms of service are declined, then the account.deleteAccount method should be called with the reason "Decline ToS update"*

**Layer** : 211

```tl
help.termsOfServiceUpdate#28ecf961 expires:int terms_of_service:help.TermsOfService = help.TermsOfServiceUpdate;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>expires</mark> | [`int`](type/int) | New TOS updates will have to be queried using help.getTermsOfServiceUpdate in expires seconds |
| <mark>terms_of_service</mark> | [`help.TermsOfService`](type/help.TermsOfService) | New terms of service |

---

## Type

[help.TermsOfServiceUpdate](type/help.TermsOfServiceUpdate)

---

## Example

```php
$helpTermsOfServiceUpdate = $client->help->termsOfServiceUpdate(
	expires : 20,
	terms_of_service : $client->help->termsOfService(
		popup : true,
		id : $client->dataJSON(
			data : 'UnSdYgIQ89zKq7EL',
		),
		text : 'qyipCfFxPzL047lh',
		entities : array(
			$client->messageEntityUnknown(
				offset : 35,
				length : 42,
			),
			$client->messageEntityMention(
				offset : 80,
				length : 5,
			),
			$client->messageEntityHashtag(
				offset : 11,
				length : 35,
			),
			$client->messageEntityBotCommand(
				offset : 56,
				length : 89,
			),
			$client->messageEntityUrl(
				offset : 39,
				length : 60,
			),
			$client->messageEntityEmail(
				offset : 51,
				length : 22,
			),
			$client->messageEntityBold(
				offset : 88,
				length : 27,
			),
			$client->messageEntityItalic(
				offset : 11,
				length : 64,
			),
			$client->messageEntityCode(
				offset : 5,
				length : 75,
			),
			$client->messageEntityPre(
				offset : 20,
				length : 95,
				language : 'H78GetlSQi2NFywU',
			),
			$client->messageEntityTextUrl(
				offset : 25,
				length : 19,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 96,
				length : 85,
				user_id : 5211602311015289477,
			),
			$client->inputMessageEntityMentionName(
				offset : 82,
				length : 32,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 85,
				length : 6,
			),
			$client->messageEntityCashtag(
				offset : 7,
				length : 55,
			),
			$client->messageEntityUnderline(
				offset : 34,
				length : 33,
			),
			$client->messageEntityStrike(
				offset : 62,
				length : 28,
			),
			$client->messageEntityBankCard(
				offset : 5,
				length : 50,
			),
			$client->messageEntitySpoiler(
				offset : 20,
				length : 20,
			),
			$client->messageEntityCustomEmoji(
				offset : 31,
				length : 43,
				document_id : 5132391073312818264,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 65,
				length : 21,
			),
		),
		min_age_confirm : 93,
	),
);
```