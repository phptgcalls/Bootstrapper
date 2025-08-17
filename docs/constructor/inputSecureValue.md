# inputSecureValue

**Description** : *Secure value, for more info see the passport docs »*

**Layer** : 211

```tl
inputSecureValue#db21d0a7 flags:# type:SecureValueType data:flags.0?SecureData front_side:flags.1?InputSecureFile reverse_side:flags.2?InputSecureFile selfie:flags.3?InputSecureFile translation:flags.6?Vector<InputSecureFile> files:flags.4?Vector<InputSecureFile> plain_data:flags.5?SecurePlainData = InputSecureValue;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>type</mark> | [`SecureValueType`](type/SecureValueType) | Secure passport value type |
| **data** | [`flags.0?SecureData`](type/SecureData) | Encrypted Telegram Passport element data |
| **front_side** | [`flags.1?InputSecureFile`](type/InputSecureFile) | Encrypted passport file with the front side of the document |
| **reverse_side** | [`flags.2?InputSecureFile`](type/InputSecureFile) | Encrypted passport file with the reverse side of the document |
| **selfie** | [`flags.3?InputSecureFile`](type/InputSecureFile) | Encrypted passport file with a selfie of the user holding the document |
| **translation** | [`flags.6?Vector<InputSecureFile>`](type/InputSecureFile) | Array of encrypted passport files with translated versions of the provided documents |
| **files** | [`flags.4?Vector<InputSecureFile>`](type/InputSecureFile) | Array of encrypted passport files with photos the of the documents |
| **plain_data** | [`flags.5?SecurePlainData`](type/SecurePlainData) | Plaintext verified passport data |

---

## Type

[InputSecureValue](type/InputSecureValue)

---

## Example

```php
$inputSecureValue = $client->inputSecureValue(
	type : $client->secureValueTypePersonalDetails(),
	data : $client->secureData(
		data : '?7U\\LiveProto?2IJ?',
		data_hash : 'If??LiveProtoa?f7',
		secret : '1???LiveProtoOIM#,',
	),
	front_side : $client->inputSecureFileUploaded(
		id : 4829274193315184733,
		parts : 58,
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
		file_hash : '???ܜLiveProto2?&t',
		secret : '??Ȣ.LiveProto??',
	),
	reverse_side : $client->inputSecureFileUploaded(
		id : 3853071834351050238,
		parts : 1,
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
		file_hash : 'q{QLiveProto?????',
		secret : '??7?LiveProto??v',
	),
	selfie : $client->inputSecureFileUploaded(
		id : -5072817638525721501,
		parts : 16,
		md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
		file_hash : 't?AjbLiveProto?X?Cy',
		secret : 'B*Ɩ#LiveProtoG' . "\0" . '1??',
	),
	translation : array(
		$client->inputSecureFileUploaded(
			id : -5708209950557515110,
			parts : 56,
			md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			file_hash : '?|?yLiveProto)?Im)',
			secret : '?k?ۨLiveProto???',
		),
		$client->inputSecureFile(
			id : -7537279675859004567,
			access_hash : 2224349325078222987,
		),
	),
	files : array(
		$client->inputSecureFileUploaded(
			id : 5201656749155231702,
			parts : 19,
			md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			file_hash : '???iLiveProtoCj?',
			secret : '??;?LiveProto4A??',
		),
		$client->inputSecureFile(
			id : -418245254768135372,
			access_hash : -5435488368251485937,
		),
	),
	plain_data : $client->securePlainPhone(
		phone : '+1234567890',
	),
);
```