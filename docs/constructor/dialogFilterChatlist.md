# dialogFilterChatlist

**Description** : *A folder imported using a chat folder deep link »*

**Layer** : 211

```tl
dialogFilterChatlist#96537bd7 flags:# has_my_invites:flags.26?true title_noanimate:flags.28?true id:int title:TextWithEntities emoticon:flags.25?string color:flags.27?int pinned_peers:Vector<InputPeer> include_peers:Vector<InputPeer> = DialogFilter;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **has_my_invites** | [`flags.26?true`](type/true) | Whether the current user has created some chat folder deep links » to share the folder as well |
| **title_noanimate** | [`flags.28?true`](type/true) | NOTHING |
| <mark>id</mark> | [`int`](type/int) | ID of the folder |
| <mark>title</mark> | [`TextWithEntities`](type/TextWithEntities) | Name of the folder (max 12 UTF-8 chars) |
| **emoticon** | [`flags.25?string`](type/string) | Emoji to use as icon for the folder |
| **color** | [`flags.27?int`](type/int) | A color ID for the folder tag associated to this folder, see here » for more info |
| <mark>pinned_peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | Pinned chats, folders can have unlimited pinned chats |
| <mark>include_peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | Chats to include in the folder |

---

## Type

[DialogFilter](type/DialogFilter)

---

## Example

```php
$dialogFilter = $client->dialogFilterChatlist(
	has_my_invites : true,
	title_noanimate : true,
	id : 6,
	title : $client->textWithEntities(
		text : '2WmgfvNBwy3jLknG',
		entities : array(
			$client->messageEntityUnknown(
				offset : 58,
				length : 37,
			),
			$client->messageEntityMention(
				offset : 81,
				length : 21,
			),
			$client->messageEntityHashtag(
				offset : 47,
				length : 22,
			),
			$client->messageEntityBotCommand(
				offset : 35,
				length : 85,
			),
			$client->messageEntityUrl(
				offset : 0,
				length : 45,
			),
			$client->messageEntityEmail(
				offset : 22,
				length : 91,
			),
			$client->messageEntityBold(
				offset : 61,
				length : 40,
			),
			$client->messageEntityItalic(
				offset : 35,
				length : 69,
			),
			$client->messageEntityCode(
				offset : 84,
				length : 97,
			),
			$client->messageEntityPre(
				offset : 45,
				length : 12,
				language : '0KxmctkR8yeFNMfG',
			),
			$client->messageEntityTextUrl(
				offset : 96,
				length : 38,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 40,
				length : 85,
				user_id : -2005818758429644198,
			),
			$client->inputMessageEntityMentionName(
				offset : 9,
				length : 69,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 2,
				length : 46,
			),
			$client->messageEntityCashtag(
				offset : 75,
				length : 83,
			),
			$client->messageEntityUnderline(
				offset : 75,
				length : 95,
			),
			$client->messageEntityStrike(
				offset : 5,
				length : 37,
			),
			$client->messageEntityBankCard(
				offset : 72,
				length : 3,
			),
			$client->messageEntitySpoiler(
				offset : 37,
				length : 69,
			),
			$client->messageEntityCustomEmoji(
				offset : 93,
				length : 74,
				document_id : 6621810940317408768,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 93,
				length : 19,
			),
		),
	),
	emoticon : 'AGSbv4iUhO9TLV7m',
	color : 41,
	pinned_peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : 1856977509886530203,
		),
		$client->inputPeerUser(
			user_id : -4470255939648163954,
			access_hash : 5579897580451265544,
		),
		$client->inputPeerChannel(
			channel_id : -367168746488728188,
			access_hash : -1413987421364364230,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 38,
			user_id : 6522421868694234314,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 54,
			channel_id : 4783705035844289814,
		),
	),
	include_peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : 3579770198694900817,
		),
		$client->inputPeerUser(
			user_id : -6061529337357321427,
			access_hash : -5066400753458955797,
		),
		$client->inputPeerChannel(
			channel_id : -4192243965094403555,
			access_hash : -1554232886442197714,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 3,
			user_id : 5731648692756978114,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 50,
			channel_id : -109983980320218388,
		),
	),
);
```