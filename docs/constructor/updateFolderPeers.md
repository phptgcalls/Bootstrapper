# updateFolderPeers

**Description** : *The peer list of a peer folder was updated*

**Layer** : 211

```tl
updateFolderPeers#19360dc0 folder_peers:Vector<FolderPeer> pts:int pts_count:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>folder_peers</mark> | [`Vector<FolderPeer>`](type/FolderPeer) | New peer list |
| <mark>pts</mark> | [`int`](type/int) | Event count after generation |
| <mark>pts_count</mark> | [`int`](type/int) | Number of events that were generated |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateFolderPeers(
	folder_peers : array(
		$client->folderPeer(
			peer : $client->peerUser(
				user_id : -9165684683561254595,
			),
			folder_id : 65,
		),
	),
	pts : 61,
	pts_count : 36,
);
```