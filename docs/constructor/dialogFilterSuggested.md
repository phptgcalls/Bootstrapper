# dialogFilterSuggested

**Description** : *Suggested folders*

**Layer** : 211

```tl
dialogFilterSuggested#77744d4a filter:DialogFilter description:string = DialogFilterSuggested;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>filter</mark> | [`DialogFilter`](type/DialogFilter) | Folder info |
| <mark>description</mark> | [`string`](type/string) | Folder description |

---

## Type

[DialogFilterSuggested](type/DialogFilterSuggested)

---

## Example

```php
$dialogFilterSuggested = $client->dialogFilterSuggested(
	filter : $client->dialogFilter(
		contacts : true,
		non_contacts : true,
		groups : true,
		broadcasts : true,
		bots : true,
		exclude_muted : true,
		exclude_read : true,
		exclude_archived : true,
		title_noanimate : true,
		id : 81,
		title : $client->textWithEntities(
			text : 'klowh6jOa89Xp5Sn',
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
		emoticon : 'wQCsnTfBOXop85Pi',
		color : 69,
		pinned_peers : array(
			$client->inputPeerEmpty(),
			$client->inputPeerSelf(),
			$client->inputPeerChat(
				chat_id : -4390940403260169802,
			),
			$client->inputPeerUser(
				user_id : -1640444740542626635,
				access_hash : -4760138749871278594,
			),
			$client->inputPeerChannel(
				channel_id : 6489796746883730697,
				access_hash : 1369857408584031476,
			),
			$client->inputPeerUserFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 49,
				user_id : -5376318938403119819,
			),
			$client->inputPeerChannelFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 7,
				channel_id : -5842275342606123083,
			),
		),
		include_peers : array(
			$client->inputPeerEmpty(),
			$client->inputPeerSelf(),
			$client->inputPeerChat(
				chat_id : 493348539156448306,
			),
			$client->inputPeerUser(
				user_id : 4670241814865932155,
				access_hash : -7222908070159379296,
			),
			$client->inputPeerChannel(
				channel_id : 4421634846701538942,
				access_hash : -7473630343349078906,
			),
			$client->inputPeerUserFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 90,
				user_id : 7398259093057670069,
			),
			$client->inputPeerChannelFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 42,
				channel_id : 5715533783254573536,
			),
		),
		exclude_peers : array(
			$client->inputPeerEmpty(),
			$client->inputPeerSelf(),
			$client->inputPeerChat(
				chat_id : 8716498013487028442,
			),
			$client->inputPeerUser(
				user_id : 2191113322285439025,
				access_hash : -2297285229103991851,
			),
			$client->inputPeerChannel(
				channel_id : -5876952562700342260,
				access_hash : -108039600515619026,
			),
			$client->inputPeerUserFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 52,
				user_id : 3315756977969970253,
			),
			$client->inputPeerChannelFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 84,
				channel_id : -6712212595378840924,
			),
		),
	),
	description : 'OgPbod4cR3lIzDm1',
);
```