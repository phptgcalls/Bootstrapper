# inputStorePaymentPremiumGiftCode

**Description** : *Used to gift Telegram Premium subscriptions only to some specific subscribers of a channel/supergroup or to some of our contacts, see here » for more info on giveaways and gifts*

**Layer** : 211

```tl
inputStorePaymentPremiumGiftCode#fb790393 flags:# users:Vector<InputUser> boost_peer:flags.0?InputPeer currency:string amount:long message:flags.1?TextWithEntities = InputStorePaymentPurpose;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>users</mark> | [`Vector<InputUser>`](type/InputUser) | The users that will receive the Telegram Premium subscriptions |
| **boost_peer** | [`flags.0?InputPeer`](type/InputPeer) | If set, the gifts will be sent on behalf of a channel/supergroup we are an admin of, which will also assign some boosts to it. Otherwise, the gift will be sent directly from the currently logged in user, and we will gain some extra boost slots. See here » for more info on giveaways and gifts |
| <mark>currency</mark> | [`string`](type/string) | Three-letter ISO 4217 currency code |
| <mark>amount</mark> | [`long`](type/long) | Total price in the smallest units of the currency (integer, not float/double). For example, for a price of US$ 1.45 pass amount = 145. See the exp parameter in currencies.json, it shows the number of digits past the decimal point for each currency (2 for the majority of currencies) |
| **message** | [`flags.1?TextWithEntities`](type/TextWithEntities) | Message attached with the gift |

---

## Type

[InputStorePaymentPurpose](type/InputStorePaymentPurpose)

---

## Example

```php
$inputStorePaymentPurpose = $client->inputStorePaymentPremiumGiftCode(
	users : array(
		$client->inputUserEmpty(),
		$client->inputUserSelf(),
		$client->inputUser(
			user_id : -8241169037205815777,
			access_hash : -2433724560276521118,
		),
		$client->inputUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 92,
			user_id : 6568870357027122315,
		),
	),
	boost_peer : $client->inputPeerEmpty(),
	currency : 'D5kETwQ0moqxN9vM',
	amount : -7087970595676169091,
	message : $client->textWithEntities(
		text : 'ry0dsxSnGl4uTARj',
		entities : array(
			$client->messageEntityUnknown(
				offset : 4,
				length : 87,
			),
			$client->messageEntityMention(
				offset : 30,
				length : 47,
			),
			$client->messageEntityHashtag(
				offset : 68,
				length : 30,
			),
			$client->messageEntityBotCommand(
				offset : 9,
				length : 43,
			),
			$client->messageEntityUrl(
				offset : 65,
				length : 55,
			),
			$client->messageEntityEmail(
				offset : 79,
				length : 8,
			),
			$client->messageEntityBold(
				offset : 69,
				length : 90,
			),
			$client->messageEntityItalic(
				offset : 90,
				length : 8,
			),
			$client->messageEntityCode(
				offset : 3,
				length : 37,
			),
			$client->messageEntityPre(
				offset : 84,
				length : 75,
				language : 'cuX5mOqCQil3dpYB',
			),
			$client->messageEntityTextUrl(
				offset : 65,
				length : 40,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 44,
				length : 81,
				user_id : -9138370024226513649,
			),
			$client->inputMessageEntityMentionName(
				offset : 0,
				length : 67,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 35,
				length : 26,
			),
			$client->messageEntityCashtag(
				offset : 26,
				length : 0,
			),
			$client->messageEntityUnderline(
				offset : 90,
				length : 32,
			),
			$client->messageEntityStrike(
				offset : 43,
				length : 45,
			),
			$client->messageEntityBankCard(
				offset : 35,
				length : 64,
			),
			$client->messageEntitySpoiler(
				offset : 87,
				length : 71,
			),
			$client->messageEntityCustomEmoji(
				offset : 87,
				length : 29,
				document_id : -5852473457153381431,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 62,
				length : 67,
			),
		),
	),
);
```