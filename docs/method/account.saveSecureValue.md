# account.saveSecureValue

**Description** : *Securely save Telegram Passport document, for more info see the passport docs »*

**Layer** : 211

```tl
account.saveSecureValue#899fe31d value:InputSecureValue secure_secret_id:long = SecureValue;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>value</mark> | [`InputSecureValue`](type/InputSecureValue) | Secure value, for more info see the passport docs » |
| <mark>secure_secret_id</mark> | [`long`](type/long) | Passport secret hash, for more info see the passport docs » |

---

## Result

[SecureValue](type/SecureValue)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **PASSWORD_REQUIRED** | `400` | A 2FA password must be configured to use Telegram Passport |
| **SECURE_SECRET_REQUIRED** | `400` | A secure secret is required |

---

## Example

```php
$secureValue = $client->account->saveSecureValue(
	value : $client->inputSecureValue(
		type : $client->secureValueTypePersonalDetails(),
		data : $client->secureData(
			data : '~?"hLiveProtoX??b',
			data_hash : 'j???LiveProto?{??',
			secret : 'x???LiveProto?	?' . "\0" . '.',
		),
		front_side : $client->inputSecureFileUploaded(
			id : 2138859944229134134,
			parts : 3,
			md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			file_hash : '??~?LiveProto?]?{y',
			secret : '{??	LiveProto?9??',
		),
		reverse_side : $client->inputSecureFileUploaded(
			id : -1024753248966971514,
			parts : 58,
			md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			file_hash : '???M?LiveProtou????',
			secret : '?\\??WLiveProto??L??',
		),
		selfie : $client->inputSecureFileUploaded(
			id : -5217255555962397348,
			parts : 78,
			md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
			file_hash : '??փLiveProto0?$\'',
			secret : 'Rⲟ?LiveProto???',
		),
		translation : array(
			$client->inputSecureFileUploaded(
				id : -8598153042721259114,
				parts : 86,
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
				file_hash : '/?<?TLiveProto??7?9',
				secret : '????LiveProto??Ga+',
			),
			$client->inputSecureFile(
				id : -1284080751603164496,
				access_hash : 1944428123646044502,
			),
		),
		files : array(
			$client->inputSecureFileUploaded(
				id : -1372634668467077887,
				parts : 74,
				md5_checksum : 'b362bee8a21feedcbd20d5b0bef421e4',
				file_hash : 'ۉm??LiveProto????',
				secret : '???zLiveProto?O;w?',
			),
			$client->inputSecureFile(
				id : 3800280382073021838,
				access_hash : 3377931946358580848,
			),
		),
		plain_data : $client->securePlainPhone(
			phone : '+1234567890',
		),
	),
	secure_secret_id : 8461166118579396440,
);
```