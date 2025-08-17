# inputInvoiceStarGift

**Description** : *Used to buy a Telegram Star Gift, see here » for more info*

**Layer** : 211

```tl
inputInvoiceStarGift#e8625e92 flags:# hide_name:flags.0?true include_upgrade:flags.2?true peer:InputPeer gift_id:long message:flags.1?TextWithEntities = InputInvoice;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **hide_name** | [`flags.0?true`](type/true) | If set, your name will be hidden if the destination user decides to display the gift on their profile (they will still see that you sent the gift) |
| **include_upgrade** | [`flags.2?true`](type/true) | NOTHING |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | NOTHING |
| <mark>gift_id</mark> | [`long`](type/long) | Identifier of the gift, from starGift.id |
| **message** | [`flags.1?TextWithEntities`](type/TextWithEntities) | Optional message, attached with the gift. The maximum length for this field is specified in the stargifts_message_length_max client configuration value » |

---

## Type

[InputInvoice](type/InputInvoice)

---

## Example

```php
$inputInvoice = $client->inputInvoiceStarGift(
	hide_name : true,
	include_upgrade : true,
	peer : $client->inputPeerEmpty(),
	gift_id : -7472695770741019762,
	message : $client->textWithEntities(
		text : 'wdLVF8CJeRUojBNP',
		entities : array(
			$client->messageEntityUnknown(
				offset : 92,
				length : 81,
			),
			$client->messageEntityMention(
				offset : 99,
				length : 94,
			),
			$client->messageEntityHashtag(
				offset : 73,
				length : 33,
			),
			$client->messageEntityBotCommand(
				offset : 21,
				length : 75,
			),
			$client->messageEntityUrl(
				offset : 95,
				length : 7,
			),
			$client->messageEntityEmail(
				offset : 43,
				length : 92,
			),
			$client->messageEntityBold(
				offset : 71,
				length : 94,
			),
			$client->messageEntityItalic(
				offset : 36,
				length : 75,
			),
			$client->messageEntityCode(
				offset : 32,
				length : 26,
			),
			$client->messageEntityPre(
				offset : 20,
				length : 12,
				language : '6cVC1IJhsEMymiDo',
			),
			$client->messageEntityTextUrl(
				offset : 7,
				length : 18,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 5,
				length : 91,
				user_id : 3653599895151501829,
			),
			$client->inputMessageEntityMentionName(
				offset : 65,
				length : 7,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 0,
				length : 74,
			),
			$client->messageEntityCashtag(
				offset : 1,
				length : 15,
			),
			$client->messageEntityUnderline(
				offset : 17,
				length : 57,
			),
			$client->messageEntityStrike(
				offset : 83,
				length : 15,
			),
			$client->messageEntityBankCard(
				offset : 49,
				length : 31,
			),
			$client->messageEntitySpoiler(
				offset : 52,
				length : 22,
			),
			$client->messageEntityCustomEmoji(
				offset : 58,
				length : 24,
				document_id : -655794988137715130,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 71,
				length : 78,
			),
		),
	),
);
```