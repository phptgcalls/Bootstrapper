# account.createBusinessChatLink

**Description** : *Create a business chat deep link »*

**Layer** : 211

```tl
account.createBusinessChatLink#8851e68e link:InputBusinessChatLink = BusinessChatLink;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>link</mark> | [`InputBusinessChatLink`](type/InputBusinessChatLink) | Info about the link to create |

---

## Result

[BusinessChatLink](type/BusinessChatLink)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHATLINKS_TOO_MUCH** | `400` | Too many business chat links were created, please delete some older links |
| **PREMIUM_ACCOUNT_REQUIRED** | `403` | A premium account is required to execute this action |

---

## Example

```php
$businessChatLink = $client->account->createBusinessChatLink(
	link : $client->inputBusinessChatLink(
		message : 'uFdGrWoHvyXMjmQ7',
		entities : array(
			$client->messageEntityUnknown(
				offset : 77,
				length : 99,
			),
			$client->messageEntityMention(
				offset : 26,
				length : 70,
			),
			$client->messageEntityHashtag(
				offset : 15,
				length : 58,
			),
			$client->messageEntityBotCommand(
				offset : 34,
				length : 38,
			),
			$client->messageEntityUrl(
				offset : 22,
				length : 32,
			),
			$client->messageEntityEmail(
				offset : 18,
				length : 58,
			),
			$client->messageEntityBold(
				offset : 88,
				length : 9,
			),
			$client->messageEntityItalic(
				offset : 65,
				length : 40,
			),
			$client->messageEntityCode(
				offset : 33,
				length : 72,
			),
			$client->messageEntityPre(
				offset : 6,
				length : 22,
				language : 'c4eajFXJY78koDUE',
			),
			$client->messageEntityTextUrl(
				offset : 94,
				length : 59,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 27,
				length : 39,
				user_id : -4861478706687672054,
			),
			$client->inputMessageEntityMentionName(
				offset : 20,
				length : 33,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 74,
				length : 68,
			),
			$client->messageEntityCashtag(
				offset : 58,
				length : 10,
			),
			$client->messageEntityUnderline(
				offset : 99,
				length : 94,
			),
			$client->messageEntityStrike(
				offset : 39,
				length : 89,
			),
			$client->messageEntityBankCard(
				offset : 65,
				length : 55,
			),
			$client->messageEntitySpoiler(
				offset : 11,
				length : 53,
			),
			$client->messageEntityCustomEmoji(
				offset : 1,
				length : 58,
				document_id : 6315051540817321564,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 15,
				length : 50,
			),
		),
		title : '3akOxcgF04ISmquE',
	),
);
```