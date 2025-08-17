# messages.sendEncryptedFile

**Description** : *Sends a message with a file attachment to a secret chat*

**Layer** : 211

```tl
messages.sendEncryptedFile#5559481d flags:# silent:flags.0?true peer:InputEncryptedChat random_id:long data:bytes file:InputEncryptedFile = messages.SentEncryptedMessage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **silent** | [`flags.0?true`](type/true) | Whether to send the file without triggering a notification |
| <mark>peer</mark> | [`InputEncryptedChat`](type/InputEncryptedChat) | Secret chat ID |
| <mark>random_id</mark> | [`long`](type/long) | Unique client message ID necessary to prevent message resending |
| <mark>data</mark> | [`bytes`](type/bytes) | TL-serialization of DecryptedMessage type, encrypted with a key generated during chat initialization |
| <mark>file</mark> | [`InputEncryptedFile`](type/InputEncryptedFile) | File attachment for the secret chat |

---

## Result

[messages.SentEncryptedMessage](type/messages.SentEncryptedMessage)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **CHAT_ID_INVALID** | `400` | The provided chat id is invalid |
| **DATA_TOO_LONG** | `400` | Data too long |
| **ENCRYPTION_DECLINED** | `400` | The secret chat was declined |
| **FILE_EMTPY** | `400` | An empty file was provided |
| **MD5_CHECKSUM_INVALID** | `400` | The MD5 checksums do not match |
| **MSG_WAIT_FAILED** | `400` | A waiting call returned an error |

---

## Example

```php
$messagesSentEncryptedMessage = $client->messages->sendEncryptedFile(
	silent : true,
	peer : $client->inputEncryptedChat(
		chat_id : 23,
		access_hash : -1806284749553190391,
	),
	random_id : -6769677476953480610,
	data : 'h?oxvLiveProto???]?',
	file : $client->inputEncryptedFileEmpty(),
);
```