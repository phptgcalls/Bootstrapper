# messages.editFactCheck

**Description** : *Edit/create a fact-check on a message*

**Layer** : 211

```tl
messages.editFactCheck#589ee75 peer:InputPeer msg_id:int text:TextWithEntities = Updates;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Peer where the message was sent |
| <mark>msg_id</mark> | [`int`](type/int) | Message ID |
| <mark>text</mark> | [`TextWithEntities`](type/TextWithEntities) | Fact-check (maximum UTF-8 length specified in appConfig.factcheck_length_limit) |

---

## Result

[Updates](type/Updates)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHAT_ACTION_FORBIDDEN** | `403` | You cannot execute this action |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$updates = $client->messages->editFactCheck(
	peer : $client->inputPeerEmpty(),
	msg_id : 96,
	text : $client->textWithEntities(
		text : 'vnPF6NHaeiwV5c18',
		entities : array(
			$client->messageEntityUnknown(
				offset : 54,
				length : 100,
			),
			$client->messageEntityMention(
				offset : 78,
				length : 82,
			),
			$client->messageEntityHashtag(
				offset : 70,
				length : 80,
			),
			$client->messageEntityBotCommand(
				offset : 4,
				length : 47,
			),
			$client->messageEntityUrl(
				offset : 26,
				length : 27,
			),
			$client->messageEntityEmail(
				offset : 72,
				length : 11,
			),
			$client->messageEntityBold(
				offset : 85,
				length : 90,
			),
			$client->messageEntityItalic(
				offset : 56,
				length : 30,
			),
			$client->messageEntityCode(
				offset : 42,
				length : 79,
			),
			$client->messageEntityPre(
				offset : 38,
				length : 65,
				language : 'LEi2xTkahced3S0K',
			),
			$client->messageEntityTextUrl(
				offset : 69,
				length : 20,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 71,
				length : 4,
				user_id : 1573116624984712722,
			),
			$client->inputMessageEntityMentionName(
				offset : 35,
				length : 87,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 26,
				length : 82,
			),
			$client->messageEntityCashtag(
				offset : 67,
				length : 15,
			),
			$client->messageEntityUnderline(
				offset : 20,
				length : 10,
			),
			$client->messageEntityStrike(
				offset : 97,
				length : 50,
			),
			$client->messageEntityBankCard(
				offset : 37,
				length : 44,
			),
			$client->messageEntitySpoiler(
				offset : 13,
				length : 85,
			),
			$client->messageEntityCustomEmoji(
				offset : 27,
				length : 77,
				document_id : -5419567708466934524,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 52,
				length : 24,
			),
		),
	),
);
```