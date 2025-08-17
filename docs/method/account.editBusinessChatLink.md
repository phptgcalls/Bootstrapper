# account.editBusinessChatLink

**Description** : *Edit a created business chat deep link »*

**Layer** : 211

```tl
account.editBusinessChatLink#8c3410af slug:string link:InputBusinessChatLink = BusinessChatLink;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>slug</mark> | [`string`](type/string) | Slug of the link, obtained as specified here » |
| <mark>link</mark> | [`InputBusinessChatLink`](type/InputBusinessChatLink) | New link information |

---

## Result

[BusinessChatLink](type/BusinessChatLink)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHATLINK_SLUG_EMPTY** | `400` | The specified slug is empty |
| **PREMIUM_ACCOUNT_REQUIRED** | `403` | A premium account is required to execute this action |

---

## Example

```php
$businessChatLink = $client->account->editBusinessChatLink(
	slug : 'qe1uhQ4UZsBTCnFI',
	link : $client->inputBusinessChatLink(
		message : 'OQbC1DRmHdMgwK4e',
		entities : array(
			$client->messageEntityUnknown(
				offset : 98,
				length : 42,
			),
			$client->messageEntityMention(
				offset : 63,
				length : 92,
			),
			$client->messageEntityHashtag(
				offset : 6,
				length : 37,
			),
			$client->messageEntityBotCommand(
				offset : 80,
				length : 68,
			),
			$client->messageEntityUrl(
				offset : 44,
				length : 44,
			),
			$client->messageEntityEmail(
				offset : 38,
				length : 48,
			),
			$client->messageEntityBold(
				offset : 31,
				length : 65,
			),
			$client->messageEntityItalic(
				offset : 92,
				length : 43,
			),
			$client->messageEntityCode(
				offset : 35,
				length : 25,
			),
			$client->messageEntityPre(
				offset : 17,
				length : 44,
				language : '6SqU2M53XNRDxaeC',
			),
			$client->messageEntityTextUrl(
				offset : 8,
				length : 99,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 35,
				length : 53,
				user_id : 154823264002027193,
			),
			$client->inputMessageEntityMentionName(
				offset : 92,
				length : 57,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 89,
				length : 1,
			),
			$client->messageEntityCashtag(
				offset : 54,
				length : 8,
			),
			$client->messageEntityUnderline(
				offset : 22,
				length : 39,
			),
			$client->messageEntityStrike(
				offset : 32,
				length : 37,
			),
			$client->messageEntityBankCard(
				offset : 37,
				length : 14,
			),
			$client->messageEntitySpoiler(
				offset : 68,
				length : 38,
			),
			$client->messageEntityCustomEmoji(
				offset : 41,
				length : 47,
				document_id : 7665502323066731415,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 71,
				length : 71,
			),
		),
		title : 'H8gtyzOscXbLJIp9',
	),
);
```