# secureValue

**Description** : *Secure value*

**Layer** : 211

```tl
secureValue#187fa0ca flags:# type:SecureValueType data:flags.0?SecureData front_side:flags.1?SecureFile reverse_side:flags.2?SecureFile selfie:flags.3?SecureFile translation:flags.6?Vector<SecureFile> files:flags.4?Vector<SecureFile> plain_data:flags.5?SecurePlainData hash:bytes = SecureValue;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>type</mark> | [`SecureValueType`](type/SecureValueType) | Secure passport value type |
| **data** | [`flags.0?SecureData`](type/SecureData) | Encrypted Telegram Passport element data |
| **front_side** | [`flags.1?SecureFile`](type/SecureFile) | Encrypted passport file with the front side of the document |
| **reverse_side** | [`flags.2?SecureFile`](type/SecureFile) | Encrypted passport file with the reverse side of the document |
| **selfie** | [`flags.3?SecureFile`](type/SecureFile) | Encrypted passport file with a selfie of the user holding the document |
| **translation** | [`flags.6?Vector<SecureFile>`](type/SecureFile) | Array of encrypted passport files with translated versions of the provided documents |
| **files** | [`flags.4?Vector<SecureFile>`](type/SecureFile) | Array of encrypted passport files with photos the of the documents |
| **plain_data** | [`flags.5?SecurePlainData`](type/SecurePlainData) | Plaintext verified passport data |
| <mark>hash</mark> | [`bytes`](type/bytes) | Data hash |

---

## Type

[SecureValue](type/SecureValue)

---

## Example

```php
$secureValue = $client->secureValue(
	type : $client->secureValueTypePersonalDetails(),
	data : $client->secureData(
		data : '?!?
?LiveProto??[?',
		data_hash : '' . "\0" . '^~LiveProto!jĩ',
		secret : '?]"	hLiveProto?,?8',
	),
	front_side : $client->secureFileEmpty(),
	reverse_side : $client->secureFileEmpty(),
	selfie : $client->secureFileEmpty(),
	translation : array(
		$client->secureFileEmpty(),
		$client->secureFile(
			id : -5167121259033282964,
			access_hash : 753124144981103067,
			size : -8123489217617319548,
			dc_id : 35,
			date : 54,
			file_hash : '?z??LiveProto!?l?',
			secret : '?toM\\LiveProto?=?S',
		),
	),
	files : array(
		$client->secureFileEmpty(),
		$client->secureFile(
			id : 642450981138601539,
			access_hash : -1384543472050993412,
			size : -7884549316599377592,
			dc_id : 81,
			date : 38,
			file_hash : '.?=`LiveProtoRf??5',
			secret : '????SLiveProto2??O',
		),
	),
	plain_data : $client->securePlainPhone(
		phone : '+1234567890',
	),
	hash : '$??LiveProto???',
);
```