# pendingSuggestion

**Layer** : 211

```tl
pendingSuggestion#e7e82e12 suggestion:string title:TextWithEntities description:TextWithEntities url:string = PendingSuggestion;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>suggestion</mark> | [`string`](type/string) | NOTHING |
| <mark>title</mark> | [`TextWithEntities`](type/TextWithEntities) | NOTHING |
| <mark>description</mark> | [`TextWithEntities`](type/TextWithEntities) | NOTHING |
| <mark>url</mark> | [`string`](type/string) | NOTHING |

---

## Type

[PendingSuggestion](type/PendingSuggestion)

---

## Example

```php
$pendingSuggestion = $client->pendingSuggestion(
	suggestion : 'cAxT5OML2bgDVwh1',
	title : $client->textWithEntities(
		text : 'KsuR1vnJy9zZ62kq',
		entities : array(
			$client->messageEntityUnknown(
				offset : 69,
				length : 81,
			),
			$client->messageEntityMention(
				offset : 99,
				length : 49,
			),
			$client->messageEntityHashtag(
				offset : 6,
				length : 47,
			),
			$client->messageEntityBotCommand(
				offset : 16,
				length : 47,
			),
			$client->messageEntityUrl(
				offset : 25,
				length : 12,
			),
			$client->messageEntityEmail(
				offset : 50,
				length : 98,
			),
			$client->messageEntityBold(
				offset : 34,
				length : 12,
			),
			$client->messageEntityItalic(
				offset : 77,
				length : 40,
			),
			$client->messageEntityCode(
				offset : 11,
				length : 49,
			),
			$client->messageEntityPre(
				offset : 18,
				length : 10,
				language : 'Wl9seSj0fmIFarYz',
			),
			$client->messageEntityTextUrl(
				offset : 37,
				length : 13,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 31,
				length : 94,
				user_id : -8701610798889868627,
			),
			$client->inputMessageEntityMentionName(
				offset : 25,
				length : 51,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 19,
				length : 55,
			),
			$client->messageEntityCashtag(
				offset : 94,
				length : 63,
			),
			$client->messageEntityUnderline(
				offset : 98,
				length : 79,
			),
			$client->messageEntityStrike(
				offset : 91,
				length : 87,
			),
			$client->messageEntityBankCard(
				offset : 74,
				length : 84,
			),
			$client->messageEntitySpoiler(
				offset : 23,
				length : 91,
			),
			$client->messageEntityCustomEmoji(
				offset : 54,
				length : 65,
				document_id : 4773256504320521997,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 94,
				length : 33,
			),
		),
	),
	description : $client->textWithEntities(
		text : 'bo2u3BXmvpyMUKH1',
		entities : array(
			$client->messageEntityUnknown(
				offset : 35,
				length : 56,
			),
			$client->messageEntityMention(
				offset : 50,
				length : 4,
			),
			$client->messageEntityHashtag(
				offset : 16,
				length : 74,
			),
			$client->messageEntityBotCommand(
				offset : 42,
				length : 75,
			),
			$client->messageEntityUrl(
				offset : 0,
				length : 45,
			),
			$client->messageEntityEmail(
				offset : 35,
				length : 37,
			),
			$client->messageEntityBold(
				offset : 10,
				length : 82,
			),
			$client->messageEntityItalic(
				offset : 75,
				length : 48,
			),
			$client->messageEntityCode(
				offset : 75,
				length : 55,
			),
			$client->messageEntityPre(
				offset : 92,
				length : 93,
				language : 'GlbAZ92tKnqh1j0X',
			),
			$client->messageEntityTextUrl(
				offset : 41,
				length : 55,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 36,
				length : 28,
				user_id : -81560596557298512,
			),
			$client->inputMessageEntityMentionName(
				offset : 95,
				length : 8,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 69,
				length : 67,
			),
			$client->messageEntityCashtag(
				offset : 11,
				length : 67,
			),
			$client->messageEntityUnderline(
				offset : 46,
				length : 55,
			),
			$client->messageEntityStrike(
				offset : 16,
				length : 18,
			),
			$client->messageEntityBankCard(
				offset : 87,
				length : 11,
			),
			$client->messageEntitySpoiler(
				offset : 4,
				length : 80,
			),
			$client->messageEntityCustomEmoji(
				offset : 6,
				length : 53,
				document_id : 5554231250727564956,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 44,
				length : 78,
			),
		),
	),
	url : 'https://docs.liveproto.dev',
);
```