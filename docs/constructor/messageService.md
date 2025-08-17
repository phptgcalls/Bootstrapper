# messageService

**Description** : *Indicates a service message*

**Layer** : 211

```tl
messageService#7a800e0a flags:# out:flags.1?true mentioned:flags.4?true media_unread:flags.5?true reactions_are_possible:flags.9?true silent:flags.13?true post:flags.14?true legacy:flags.19?true id:int from_id:flags.8?Peer peer_id:Peer saved_peer_id:flags.28?Peer reply_to:flags.3?MessageReplyHeader date:int action:MessageAction reactions:flags.20?MessageReactions ttl_period:flags.25?int = Message;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **out** | [`flags.1?true`](type/true) | Whether the message is outgoing |
| **mentioned** | [`flags.4?true`](type/true) | Whether we were mentioned in the message |
| **media_unread** | [`flags.5?true`](type/true) | Whether the message contains unread media |
| **reactions_are_possible** | [`flags.9?true`](type/true) | NOTHING |
| **silent** | [`flags.13?true`](type/true) | Whether the message is silent |
| **post** | [`flags.14?true`](type/true) | Whether it's a channel post |
| **legacy** | [`flags.19?true`](type/true) | This is a legacy message: it has to be refetched with the new layer |
| <mark>id</mark> | [`int`](type/int) | Message ID |
| **from_id** | [`flags.8?Peer`](type/Peer) | ID of the sender of this message |
| <mark>peer_id</mark> | [`Peer`](type/Peer) | Sender of service message |
| **saved_peer_id** | [`flags.28?Peer`](type/Peer) | NOTHING |
| **reply_to** | [`flags.3?MessageReplyHeader`](type/MessageReplyHeader) | Reply (thread) information |
| <mark>date</mark> | [`int`](type/int) | Message date |
| <mark>action</mark> | [`MessageAction`](type/MessageAction) | Event connected with the service message |
| **reactions** | [`flags.20?MessageReactions`](type/MessageReactions) | NOTHING |
| **ttl_period** | [`flags.25?int`](type/int) | Time To Live of the message, once message.date+message.ttl_period === time(), the message will be deleted on the server, and must be deleted locally as well |

---

## Type

[Message](type/Message)

---

## Example

```php
$message = $client->messageService(
	out : true,
	mentioned : true,
	media_unread : true,
	reactions_are_possible : true,
	silent : true,
	post : true,
	legacy : true,
	id : 51,
	from_id : $client->peerUser(
		user_id : 8970340019223522985,
	),
	peer_id : $client->peerUser(
		user_id : 54488389871869913,
	),
	saved_peer_id : $client->peerUser(
		user_id : -4369702027028780935,
	),
	reply_to : $client->messageReplyHeader(
		reply_to_scheduled : true,
		forum_topic : true,
		quote : true,
		reply_to_msg_id : 17,
		reply_to_peer_id : $client->peerUser(
			user_id : -8015269200976355550,
		),
		reply_from : $client->messageFwdHeader(
			imported : true,
			saved_out : true,
			from_id : $client->peerUser(...),
			from_name : 'LndUD2OpCPXQmyjh',
			date : 37,
			channel_post : 96,
			post_author : 'sbAjWXCleGQRFSMB',
			saved_from_peer : $client->peerUser(...),
			saved_from_msg_id : 67,
			saved_from_id : $client->peerUser(...),
			saved_from_name : 'CJVTHKnbDl7uwe2z',
			saved_date : 31,
			psa_type : 'fmj3g6e5a8JuNnhO',
		),
		reply_media : $client->messageMediaEmpty(),
		reply_to_top_id : 19,
		quote_text : 'ABzh9e3RNfrvSHMo',
		quote_entities : array(
			$client->messageEntityUnknown(
				offset : 3,
				length : 97,
			),
			$client->messageEntityMention(
				offset : 80,
				length : 1,
			),
			$client->messageEntityHashtag(
				offset : 100,
				length : 16,
			),
			$client->messageEntityBotCommand(
				offset : 4,
				length : 100,
			),
			$client->messageEntityUrl(
				offset : 23,
				length : 72,
			),
			$client->messageEntityEmail(
				offset : 0,
				length : 2,
			),
			$client->messageEntityBold(
				offset : 12,
				length : 96,
			),
			$client->messageEntityItalic(
				offset : 95,
				length : 20,
			),
			$client->messageEntityCode(
				offset : 55,
				length : 36,
			),
			$client->messageEntityPre(
				offset : 5,
				length : 2,
				language : '4pulEDx2GKLRyv8q',
			),
			$client->messageEntityTextUrl(
				offset : 53,
				length : 91,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 44,
				length : 90,
				user_id : -8659031890477251596,
			),
			$client->inputMessageEntityMentionName(
				offset : 50,
				length : 23,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 65,
				length : 58,
			),
			$client->messageEntityCashtag(
				offset : 28,
				length : 32,
			),
			$client->messageEntityUnderline(
				offset : 82,
				length : 52,
			),
			$client->messageEntityStrike(
				offset : 40,
				length : 45,
			),
			$client->messageEntityBankCard(
				offset : 1,
				length : 46,
			),
			$client->messageEntitySpoiler(
				offset : 9,
				length : 60,
			),
			$client->messageEntityCustomEmoji(
				offset : 95,
				length : 92,
				document_id : 8542291968223417255,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 39,
				length : 37,
			),
		),
		quote_offset : 56,
		todo_item_id : 99,
	),
	date : 38,
	action : $client->messageActionEmpty(),
	reactions : $client->messageReactions(
		min : true,
		can_see_list : true,
		reactions_as_tags : true,
		results : array(
			$client->reactionCount(
				chosen_order : 46,
				reaction : $client->reactionEmpty(...),
				count : 15,
			),
		),
		recent_reactions : array(
			$client->messagePeerReaction(
				big : true,
				unread : true,
				my : true,
				peer_id : $client->peerUser(...),
				date : 86,
				reaction : $client->reactionEmpty(...),
			),
		),
		top_reactors : array(
			$client->messageReactor(
				top : true,
				my : true,
				anonymous : true,
				peer_id : $client->peerUser(...),
				count : 57,
			),
		),
	),
	ttl_period : 27,
);
```