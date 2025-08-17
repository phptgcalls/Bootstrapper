# chatlists.exportedChatlistInvite

**Description** : *Info about an exported chat folder deep link »*

**Layer** : 211

```tl
chatlists.exportedChatlistInvite#10e6e3a6 filter:DialogFilter invite:ExportedChatlistInvite = chatlists.ExportedChatlistInvite;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>filter</mark> | [`DialogFilter`](type/DialogFilter) | Folder ID |
| <mark>invite</mark> | [`ExportedChatlistInvite`](type/ExportedChatlistInvite) | The exported chat folder deep link » |

---

## Type

[chatlists.ExportedChatlistInvite](type/chatlists.ExportedChatlistInvite)

---

## Example

```php
$chatlistsExportedChatlistInvite = $client->chatlists->exportedChatlistInvite(
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
		id : 97,
		title : $client->textWithEntities(
			text : 'WGBCS1xm2RHbqnoO',
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
		emoticon : 'LfkGladIEJ2oN73b',
		color : 20,
		pinned_peers : array(
			$client->inputPeerEmpty(),
			$client->inputPeerSelf(),
			$client->inputPeerChat(
				chat_id : -4259605240204847655,
			),
			$client->inputPeerUser(
				user_id : 4116650906016805272,
				access_hash : 1038466741686992724,
			),
			$client->inputPeerChannel(
				channel_id : 4447024410641228445,
				access_hash : 8430468695520397194,
			),
			$client->inputPeerUserFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 35,
				user_id : 396926735163045690,
			),
			$client->inputPeerChannelFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 37,
				channel_id : -3461064481804450997,
			),
		),
		include_peers : array(
			$client->inputPeerEmpty(),
			$client->inputPeerSelf(),
			$client->inputPeerChat(
				chat_id : -8790020061717050028,
			),
			$client->inputPeerUser(
				user_id : -8671805688738947240,
				access_hash : -5752614980185965294,
			),
			$client->inputPeerChannel(
				channel_id : 3582851931169313972,
				access_hash : -156880416274138250,
			),
			$client->inputPeerUserFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 95,
				user_id : -318678317156447807,
			),
			$client->inputPeerChannelFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 7,
				channel_id : 6710267603646324010,
			),
		),
		exclude_peers : array(
			$client->inputPeerEmpty(),
			$client->inputPeerSelf(),
			$client->inputPeerChat(
				chat_id : -4743781296548699648,
			),
			$client->inputPeerUser(
				user_id : 8655874946844881200,
				access_hash : 1283335161499511022,
			),
			$client->inputPeerChannel(
				channel_id : -6827026748671385023,
				access_hash : 1584115003852165966,
			),
			$client->inputPeerUserFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 48,
				user_id : -3938757460842449097,
			),
			$client->inputPeerChannelFromMessage(
				peer : $client->inputPeerEmpty(...),
				msg_id : 62,
				channel_id : 3199308732112552978,
			),
		),
	),
	invite : $client->exportedChatlistInvite(
		title : 'Tip1XtPDMuxyCGg0',
		url : 'https://docs.liveproto.dev',
		peers : array(
			$client->peerUser(
				user_id : 5895116017187047020,
			),
			$client->peerChat(
				chat_id : -205815679072560665,
			),
			$client->peerChannel(
				channel_id : -7556772429661987943,
			),
		),
	),
);
```