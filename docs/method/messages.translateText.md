# messages.translateText

**Description** : *Translate a given text*

**Layer** : 211

```tl
messages.translateText#63183030 flags:# peer:flags.0?InputPeer id:flags.0?Vector<int> text:flags.1?Vector<TextWithEntities> to_lang:string = messages.TranslatedText;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **peer** | [`flags.0?InputPeer`](type/InputPeer) | If the text is a chat message, the peer ID |
| **id** | [`flags.0?Vector<int>`](type/int) | A list of message IDs to translate |
| **text** | [`flags.1?Vector<TextWithEntities>`](type/TextWithEntities) | A list of styled messages to translate |
| <mark>to_lang</mark> | [`string`](type/string) | Two-letter ISO 639-1 language code of the language to which the message is translated |

---

## Result

[messages.TranslatedText](type/messages.TranslatedText)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **INPUT_TEXT_EMPTY** | `400` | The specified text is empty |
| **INPUT_TEXT_TOO_LONG** | `400` | The specified text is too long |
| **MSG_ID_INVALID** | `400` | Invalid message ID provided |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |
| **TO_LANG_INVALID** | `400` | The specified destination language is invalid |
| **TRANSLATE_REQ_FAILED** | `500` | Translation failed, please try again later |
| **TRANSLATE_REQ_QUOTA_EXCEEDED** | `400` | Translation is currently unavailable due to a temporary server-side lack of resources |

---

## Example

```php
$messagesTranslatedText = $client->messages->translateText(
	peer : $client->inputPeerEmpty(),
	id : array(83),
	text : array(
		$client->textWithEntities(
			text : 'rh73EadtmgCB5xcD',
			entities : array(
				$client->messageEntityUnknown(
					offset : 32,
					length : 1,
				),
				$client->messageEntityMention(
					offset : 97,
					length : 20,
				),
				$client->messageEntityHashtag(
					offset : 40,
					length : 63,
				),
				$client->messageEntityBotCommand(
					offset : 5,
					length : 79,
				),
				$client->messageEntityUrl(
					offset : 10,
					length : 2,
				),
				$client->messageEntityEmail(
					offset : 15,
					length : 77,
				),
				$client->messageEntityBold(
					offset : 54,
					length : 13,
				),
				$client->messageEntityItalic(
					offset : 100,
					length : 29,
				),
				$client->messageEntityCode(
					offset : 17,
					length : 73,
				),
				$client->messageEntityPre(
					offset : 58,
					length : 7,
					language : 'ecbK1p7nxMRI5hJY',
				),
				$client->messageEntityTextUrl(
					offset : 42,
					length : 40,
					url : 'https://docs.liveproto.dev',
				),
				$client->messageEntityMentionName(
					offset : 98,
					length : 9,
					user_id : -6098379789722530445,
				),
				$client->inputMessageEntityMentionName(
					offset : 23,
					length : 52,
					user_id : $client->inputUserEmpty(...),
				),
				$client->messageEntityPhone(
					offset : 74,
					length : 64,
				),
				$client->messageEntityCashtag(
					offset : 86,
					length : 97,
				),
				$client->messageEntityUnderline(
					offset : 94,
					length : 49,
				),
				$client->messageEntityStrike(
					offset : 26,
					length : 29,
				),
				$client->messageEntityBankCard(
					offset : 25,
					length : 20,
				),
				$client->messageEntitySpoiler(
					offset : 38,
					length : 39,
				),
				$client->messageEntityCustomEmoji(
					offset : 46,
					length : 38,
					document_id : 7519443343598672982,
				),
				$client->messageEntityBlockquote(
					collapsed : true,
					offset : 40,
					length : 83,
				),
			),
		),
	),
	to_lang : 'WE9CSIQcwvJ2i5Vf',
);
```