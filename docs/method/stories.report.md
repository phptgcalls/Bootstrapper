# stories.report

**Description** : *Report a story*

**Layer** : 211

```tl
stories.report#19d8eb45 peer:InputPeer id:Vector<int> option:bytes message:string = ReportResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>peer</mark> | [`InputPeer`](type/InputPeer) | The peer that uploaded the story |
| <mark>id</mark> | [`Vector<int>`](type/int) | IDs of the stories to report |
| <mark>option</mark> | [`bytes`](type/bytes) | Menu option, intially empty |
| <mark>message</mark> | [`string`](type/string) | Comment for report moderation |

---

## Result

[ReportResult](type/ReportResult)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **PEER_ID_INVALID** | `400` | The provided peer id is invalid |

---

## Example

```php
$reportResult = $client->stories->report(
	peer : $client->inputPeerEmpty(),
	id : array(72),
	option : '??{?LiveProto?:?c!',
	message : 'aMQASLjJktXsYDN0',
);
```