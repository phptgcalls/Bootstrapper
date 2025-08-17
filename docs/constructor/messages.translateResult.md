# messages.translateResult

**Description** : *Translated text with entities*

**Layer** : 211

```tl
messages.translateResult#33db32f8 result:Vector<TextWithEntities> = messages.TranslatedText;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>result</mark> | [`Vector<TextWithEntities>`](type/TextWithEntities) | Text+entities, for each input message |

---

## Type

[messages.TranslatedText](type/messages.TranslatedText)

---

## Example

```php
$messagesTranslatedText = $client->messages->translateResult(
	result : array(
		$client->textWithEntities(
			text : 'ilfbp3VSg2uIHYq4',
			entities : array(
				$client->messageEntityUnknown(
					offset : 82,
					length : 34,
				),
				$client->messageEntityMention(
					offset : 78,
					length : 17,
				),
				$client->messageEntityHashtag(
					offset : 67,
					length : 68,
				),
				$client->messageEntityBotCommand(
					offset : 86,
					length : 90,
				),
				$client->messageEntityUrl(
					offset : 93,
					length : 98,
				),
				$client->messageEntityEmail(
					offset : 81,
					length : 20,
				),
				$client->messageEntityBold(
					offset : 46,
					length : 5,
				),
				$client->messageEntityItalic(
					offset : 16,
					length : 81,
				),
				$client->messageEntityCode(
					offset : 65,
					length : 79,
				),
				$client->messageEntityPre(
					offset : 18,
					length : 7,
					language : 'sq97xAZJ43SXo2gV',
				),
				$client->messageEntityTextUrl(
					offset : 45,
					length : 12,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 59,
					length : 22,
					user_id : -138410524835910516,
				),
				$client->inputMessageEntityMentionName(
					offset : 90,
					length : 82,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 12,
					length : 21,
				),
				$client->messageEntityCashtag(
					offset : 79,
					length : 41,
				),
				$client->messageEntityUnderline(
					offset : 90,
					length : 32,
				),
				$client->messageEntityStrike(
					offset : 53,
					length : 32,
				),
				$client->messageEntityBankCard(
					offset : 93,
					length : 36,
				),
				$client->messageEntitySpoiler(
					offset : 21,
					length : 23,
				),
				$client->messageEntityCustomEmoji(
					offset : 11,
					length : 68,
					document_id : -5492600561948193485,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 9,
					length : 100,
				),
			),
		),
	),
);
```