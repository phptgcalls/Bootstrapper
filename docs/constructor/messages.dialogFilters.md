# messages.dialogFilters

**Description** : *Folder and folder tags information*

**Layer** : 211

```tl
messages.dialogFilters#2ad93719 flags:# tags_enabled:flags.0?true filters:Vector<DialogFilter> = messages.DialogFilters;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **tags_enabled** | [`flags.0?true`](type/true) | Whether folder tags are enabled |
| <mark>filters</mark> | [`Vector<DialogFilter>`](type/DialogFilter) | Folders |

---

## Type

[messages.DialogFilters](type/messages.DialogFilters)

---

## Example

```php
$messagesDialogFilters = $client->messages->dialogFilters(
	tags_enabled : true,
	filters : array(
		$client->dialogFilter(
			contacts : true,
			non_contacts : true,
			groups : true,
			broadcasts : true,
			bots : true,
			exclude_muted : true,
			exclude_read : true,
			exclude_archived : true,
			title_noanimate : true,
			id : 94,
			title : $client->textWithEntities(
				text : 'tD92bE8fSjTYcw4r',
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
			emoticon : 'y5cvWz4pNeASQYil',
			color : 99,
			pinned_peers : array(
				$client->inputPeerEmpty(),
				$client->inputPeerSelf(),
				$client->inputPeerChat(
					chat_id : 2679765836337573420,
				),
				$client->inputPeerUser(
					user_id : 3156784369235219695,
					access_hash : 9184409484316165377,
				),
				$client->inputPeerChannel(
					channel_id : -2980527868529379853,
					access_hash : 2407620668931764327,
				),
				$client->inputPeerUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 10,
					user_id : 4912945913310492610,
				),
				$client->inputPeerChannelFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 87,
					channel_id : -2296745929545511341,
				),
			),
			include_peers : array(
				$client->inputPeerEmpty(),
				$client->inputPeerSelf(),
				$client->inputPeerChat(
					chat_id : 6047811371932611706,
				),
				$client->inputPeerUser(
					user_id : 7342554731110937531,
					access_hash : 5176000167072405503,
				),
				$client->inputPeerChannel(
					channel_id : 5232551507485129334,
					access_hash : 4352932929816260862,
				),
				$client->inputPeerUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 79,
					user_id : -7126854257554544892,
				),
				$client->inputPeerChannelFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 81,
					channel_id : 2324024475366247921,
				),
			),
			exclude_peers : array(
				$client->inputPeerEmpty(),
				$client->inputPeerSelf(),
				$client->inputPeerChat(
					chat_id : 3009408416588297993,
				),
				$client->inputPeerUser(
					user_id : 3131882753482478400,
					access_hash : -6690645199918276516,
				),
				$client->inputPeerChannel(
					channel_id : 2552104290135159244,
					access_hash : 7483536000684844196,
				),
				$client->inputPeerUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 2,
					user_id : -1320015252165254881,
				),
				$client->inputPeerChannelFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 20,
					channel_id : 1334739594402224170,
				),
			),
		),
		$client->dialogFilterDefault(),
		$client->dialogFilterChatlist(
			has_my_invites : true,
			title_noanimate : true,
			id : 53,
			title : $client->textWithEntities(
				text : '6XAmJ5RG48gfstbV',
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
			emoticon : '4EqNAUafh69CcPMI',
			color : 42,
			pinned_peers : array(
				$client->inputPeerEmpty(),
				$client->inputPeerSelf(),
				$client->inputPeerChat(
					chat_id : 6619812688300123253,
				),
				$client->inputPeerUser(
					user_id : -4156221430434333276,
					access_hash : 8106787853307136869,
				),
				$client->inputPeerChannel(
					channel_id : 2974235183132578840,
					access_hash : -5523619555219373968,
				),
				$client->inputPeerUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 12,
					user_id : -6299674150441191217,
				),
				$client->inputPeerChannelFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 73,
					channel_id : 3864375651250241569,
				),
			),
			include_peers : array(
				$client->inputPeerEmpty(),
				$client->inputPeerSelf(),
				$client->inputPeerChat(
					chat_id : 5876052971668986826,
				),
				$client->inputPeerUser(
					user_id : -4552699740708722119,
					access_hash : 27631083740780525,
				),
				$client->inputPeerChannel(
					channel_id : -6911633233150427672,
					access_hash : 3254244583451506089,
				),
				$client->inputPeerUserFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 78,
					user_id : 6821098701144394810,
				),
				$client->inputPeerChannelFromMessage(
					peer : $client->inputPeerEmpty(...),
					msg_id : 1,
					channel_id : 5849603880528234972,
				),
			),
		),
	),
);
```