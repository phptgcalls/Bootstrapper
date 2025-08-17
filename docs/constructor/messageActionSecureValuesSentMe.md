# messageActionSecureValuesSentMe

**Description** : *Secure telegram passport values were received*

**Layer** : 211

```tl
messageActionSecureValuesSentMe#1b287353 values:Vector<SecureValue> credentials:SecureCredentialsEncrypted = MessageAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>values</mark> | [`Vector<SecureValue>`](type/SecureValue) | Vector with information about documents and other Telegram Passport elements that were shared with the bot |
| <mark>credentials</mark> | [`SecureCredentialsEncrypted`](type/SecureCredentialsEncrypted) | Encrypted credentials required to decrypt the data |

---

## Type

[MessageAction](type/MessageAction)

---

## Example

```php
$messageAction = $client->messageActionSecureValuesSentMe(
	values : array(
		$client->secureValue(
			type : $client->secureValueTypePersonalDetails(),
			data : $client->secureData(
				data : '??n?LiveProto̫?!',
				data_hash : '
?¶LiveProto:?GB?',
				secret : '???LiveProto=???',
			),
			front_side : $client->secureFileEmpty(),
			reverse_side : $client->secureFileEmpty(),
			selfie : $client->secureFileEmpty(),
			translation : array(
				$client->secureFileEmpty(),
				$client->secureFile(
					id : 7032217596356641975,
					access_hash : 2596320787493341321,
					size : 2521678036479093990,
					dc_id : 1,
					date : 24,
					file_hash : '' . "\0" . '?EZLiveProto*6&gs',
					secret : '	^?\'2LiveProtoZ??W?',
				),
			),
			files : array(
				$client->secureFileEmpty(),
				$client->secureFile(
					id : 3603513840264073506,
					access_hash : -3403552314908993962,
					size : -7412515196346012110,
					dc_id : 6,
					date : 91,
					file_hash : '???~LiveProtoO4ou',
					secret : '?v???LiveProto?g??',
				),
			),
			plain_data : $client->securePlainPhone(
				phone : '+1234567890',
			),
			hash : '?g?mLiveProto`ȵ?<',
		),
	),
	credentials : $client->secureCredentialsEncrypted(
		data : '?)?L?LiveProto?v??',
		hash : '???k?LiveProtoj??O',
		secret : 'S?g?LiveProto??3',
	),
);
```