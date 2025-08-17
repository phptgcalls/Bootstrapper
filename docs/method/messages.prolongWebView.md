# messages.prolongWebView

**Description** : *Indicate to the server (from the user side) that the user is still using a web app*

**Layer** : 211

```tl
messages.prolongWebView#b0d81a83 flags:# silent:flags.5?true peer:InputPeer bot:InputUser query_id:long reply_to:flags.0?InputReplyTo send_as:flags.13?InputPeer = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **silent** | [`flags.5?true`](type/true) | Whether the inline message that will be sent by the bot on behalf of the user once the web app interaction is terminated should be sent silently (no notifications for the receivers) |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | Dialog where the web app was opened |
| <mark>bot</mark> | [`InputUser`](type/InputUser) | Bot that owns the web app |
| <mark>query_id</mark> | [`long`](type/long) | Web app interaction ID obtained from messages.requestWebView |
| **reply_to** | [`flags.0?InputReplyTo`](type/InputReplyTo) | If set, indicates that the inline message that will be sent by the bot on behalf of the user once the web app interaction is terminated should be sent in reply to the specified message or story |
| **send_as** | [`flags.13?InputPeer`](type/InputPeer) | Open the web app as the specified peer |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **BOT_INVALID** | `400` | This is not a valid bot |

---

## Example

```php
$bool = $client->messages->prolongWebView(
	silent : true,
	peer : $client->inputPeerEmpty(),
	bot : $client->inputUserEmpty(),
	query_id : -3005173060526054747,
	reply_to : $client->inputReplyToMessage(
		reply_to_msg_id : 68,
		top_msg_id : 7,
		reply_to_peer_id : $client->inputPeerEmpty(),
		quote_text : 'UigcjnzRpPHCDAf3',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 43,
				length : 35,
			),
			$client->messageEntityMention(
				offset : 61,
				length : 65,
			),
			$client->messageEntityHashtag(
				offset : 59,
				length : 90,
			),
			$client->messageEntityBotCommand(
				offset : 77,
				length : 39,
			),
			$client->messageEntityUrl(
				offset : 1,
				length : 84,
			),
			$client->messageEntityEmail(
				offset : 28,
				length : 17,
			),
			$client->messageEntityBold(
				offset : 82,
				length : 96,
			),
			$client->messageEntityItalic(
				offset : 86,
				length : 21,
			),
			$client->messageEntityCode(
				offset : 97,
				length : 73,
			),
			$client->messageEntityPre(
				offset : 0,
				length : 96,
				language : '9or6GRCZegFuUqxJ',
			),
			$client->messageEntityTextUrl(
				offset : 90,
				length : 85,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 61,
				length : 12,
				user_id : -620246008822140856,
			),
			$client->inputMessageEntityMentionName(
				offset : 92,
				length : 15,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 22,
				length : 5,
			),
			$client->messageEntityCashtag(
				offset : 58,
				length : 23,
			),
			$client->messageEntityUnderline(
				offset : 97,
				length : 21,
			),
			$client->messageEntityStrike(
				offset : 46,
				length : 91,
			),
			$client->messageEntityBankCard(
				offset : 32,
				length : 7,
			),
			$client->messageEntitySpoiler(
				offset : 91,
				length : 72,
			),
			$client->messageEntityCustomEmoji(
				offset : 91,
				length : 89,
				document_id : -4633072930212407444,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 23,
				length : 28,
			),
		),
		quote_offset : 20,
		monoforum_peer_id : $client->inputPeerEmpty(),
		todo_item_id : 5,
	),
	send_as : $client->inputPeerEmpty(),
);
```