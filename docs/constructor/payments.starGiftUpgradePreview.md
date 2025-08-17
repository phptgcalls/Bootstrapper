# payments.starGiftUpgradePreview

**Layer** : 211

```tl
payments.starGiftUpgradePreview#167bd90b sample_attributes:Vector<StarGiftAttribute> = payments.StarGiftUpgradePreview;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>sample_attributes</mark> | [`Vector<StarGiftAttribute>`](type/StarGiftAttribute) | NOTHING |

---

## Type

[payments.StarGiftUpgradePreview](type/payments.StarGiftUpgradePreview)

---

## Example

```php
$paymentsStarGiftUpgradePreview = $client->payments->starGiftUpgradePreview(
	sample_attributes : array(
		$client->starGiftAttributeModel(
			name : 'xGgdbCiHYDnK5Skv',
			document : $client->documentEmpty(
				id : 7390052026706997011,
			),
			rarity_permille : 89,
		),
		$client->starGiftAttributePattern(
			name : 'cb7aSL6Cus4IikFt',
			document : $client->documentEmpty(
				id : -1242754907386042783,
			),
			rarity_permille : 19,
		),
		$client->starGiftAttributeBackdrop(
			name : 'rsKzo1t5bhleSBF4',
			backdrop_id : 41,
			center_color : 39,
			edge_color : 20,
			pattern_color : 84,
			text_color : 2,
			rarity_permille : 52,
		),
		$client->starGiftAttributeOriginalDetails(
			sender_id : $client->peerUser(
				user_id : -5012700825632365783,
			),
			recipient_id : $client->peerUser(
				user_id : 281410853623363796,
			),
			date : 40,
			message : $client->textWithEntities(
				text : 'cdaDJObylAVFmrou',
				entities : array(
					$client->messageEntityUnknown(...),
					$client->messageEntityMention(...),
					$client->messageEntityHashtag(...),
					$client->messageEntityBotCommand(...),
					$client->messageEntityUrl(...),
					$client->messageEntityEmail(...),
					$client->messageEntityBold(...),
					$client->messageEntityItalic(...),
					$client->messageEntityCode(...),
					$client->messageEntityPre(...),
					$client->messageEntityTextUrl(...),
					$client->messageEntityMentionName(...),
					$client->inputMessageEntityMentionName(...),
					$client->messageEntityPhone(...),
					$client->messageEntityCashtag(...),
					$client->messageEntityUnderline(...),
					$client->messageEntityStrike(...),
					$client->messageEntityBankCard(...),
					$client->messageEntitySpoiler(...),
					$client->messageEntityCustomEmoji(...),
					$client->messageEntityBlockquote(...),
				),
			),
		),
	),
);
```