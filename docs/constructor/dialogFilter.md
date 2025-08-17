# dialogFilter

**Description** : *Dialog filter AKA folder*

**Layer** : 211

```tl
dialogFilter#aa472651 flags:# contacts:flags.0?true non_contacts:flags.1?true groups:flags.2?true broadcasts:flags.3?true bots:flags.4?true exclude_muted:flags.11?true exclude_read:flags.12?true exclude_archived:flags.13?true title_noanimate:flags.28?true id:int title:TextWithEntities emoticon:flags.25?string color:flags.27?int pinned_peers:Vector<InputPeer> include_peers:Vector<InputPeer> exclude_peers:Vector<InputPeer> = DialogFilter;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **contacts** | [`flags.0?true`](type/true) | Whether to include all contacts in this folder |
| **non_contacts** | [`flags.1?true`](type/true) | Whether to include all non-contacts in this folder |
| **groups** | [`flags.2?true`](type/true) | Whether to include all groups in this folder |
| **broadcasts** | [`flags.3?true`](type/true) | Whether to include all channels in this folder |
| **bots** | [`flags.4?true`](type/true) | Whether to include all bots in this folder |
| **exclude_muted** | [`flags.11?true`](type/true) | Whether to exclude muted chats from this folder |
| **exclude_read** | [`flags.12?true`](type/true) | Whether to exclude read chats from this folder |
| **exclude_archived** | [`flags.13?true`](type/true) | Whether to exclude archived chats from this folder |
| **title_noanimate** | [`flags.28?true`](type/true) | NOTHING |
| <mark>id</mark> | [`int`](type/int) | Folder ID |
| <mark>title</mark> | [`TextWithEntities`](type/TextWithEntities) | Folder name (max 12 UTF-8 chars) |
| **emoticon** | [`flags.25?string`](type/string) | Emoji to use as icon for the folder |
| **color** | [`flags.27?int`](type/int) | A color ID for the folder tag associated to this folder, see here » for more info |
| <mark>pinned_peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | Pinned chats, folders can have unlimited pinned chats |
| <mark>include_peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | Include the following chats in this folder |
| <mark>exclude_peers</mark> | [`Vector<InputPeer>`](type/InputPeer) | Exclude the following chats from this folder |

---

## Type

[DialogFilter](type/DialogFilter)

---

## Example

```php
$dialogFilter = $client->dialogFilter(
	contacts : true,
	non_contacts : true,
	groups : true,
	broadcasts : true,
	bots : true,
	exclude_muted : true,
	exclude_read : true,
	exclude_archived : true,
	title_noanimate : true,
	id : 36,
	title : $client->textWithEntities(
		text : 'ibVyDXmn8IO5RBA3',
		entities : array(
			$client->messageEntityUnknown(
				offset : 77,
				length : 38,
			),
			$client->messageEntityMention(
				offset : 93,
				length : 62,
			),
			$client->messageEntityHashtag(
				offset : 77,
				length : 71,
			),
			$client->messageEntityBotCommand(
				offset : 89,
				length : 99,
			),
			$client->messageEntityUrl(
				offset : 95,
				length : 16,
			),
			$client->messageEntityEmail(
				offset : 72,
				length : 38,
			),
			$client->messageEntityBold(
				offset : 57,
				length : 55,
			),
			$client->messageEntityItalic(
				offset : 35,
				length : 21,
			),
			$client->messageEntityCode(
				offset : 9,
				length : 98,
			),
			$client->messageEntityPre(
				offset : 9,
				length : 70,
				language : 'Bn639mfwquaXhFAW',
			),
			$client->messageEntityTextUrl(
				offset : 76,
				length : 75,
				url : 'https://docs.liveproto.dev',
			),
			$client->messageEntityMentionName(
				offset : 64,
				length : 65,
				user_id : 589692626935391779,
			),
			$client->inputMessageEntityMentionName(
				offset : 26,
				length : 56,
				user_id : $client->inputUserEmpty(...),
			),
			$client->messageEntityPhone(
				offset : 38,
				length : 21,
			),
			$client->messageEntityCashtag(
				offset : 71,
				length : 62,
			),
			$client->messageEntityUnderline(
				offset : 31,
				length : 55,
			),
			$client->messageEntityStrike(
				offset : 13,
				length : 74,
			),
			$client->messageEntityBankCard(
				offset : 44,
				length : 27,
			),
			$client->messageEntitySpoiler(
				offset : 63,
				length : 28,
			),
			$client->messageEntityCustomEmoji(
				offset : 14,
				length : 28,
				document_id : 2318847315219599085,
			),
			$client->messageEntityBlockquote(
				collapsed : true,
				offset : 32,
				length : 33,
			),
		),
	),
	emoticon : 'mCX9U8eBZkfWK1pg',
	color : 10,
	pinned_peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : 919100142835002532,
		),
		$client->inputPeerUser(
			user_id : -6435363427391015759,
			access_hash : 8803053984725276829,
		),
		$client->inputPeerChannel(
			channel_id : 5320793927560887380,
			access_hash : 240864595991725078,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 9,
			user_id : -9040607139368439717,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 93,
			channel_id : -8672915935772665464,
		),
	),
	include_peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : 2233016739566691753,
		),
		$client->inputPeerUser(
			user_id : -566506022699290393,
			access_hash : -3109300266318976792,
		),
		$client->inputPeerChannel(
			channel_id : -6649862957852084284,
			access_hash : -6979653220677738753,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 94,
			user_id : 6656598718784462441,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 99,
			channel_id : 3411626370385631810,
		),
	),
	exclude_peers : array(
		$client->inputPeerEmpty(),
		$client->inputPeerSelf(),
		$client->inputPeerChat(
			chat_id : 6654039261172640327,
		),
		$client->inputPeerUser(
			user_id : -1165792923484920602,
			access_hash : -6007292658578616790,
		),
		$client->inputPeerChannel(
			channel_id : -8966876048889424975,
			access_hash : 8047768876423824820,
		),
		$client->inputPeerUserFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 15,
			user_id : 1126786475988733514,
		),
		$client->inputPeerChannelFromMessage(
			peer : $client->inputPeerEmpty(),
			msg_id : 1,
			channel_id : -1880426061514341513,
		),
	),
);
```