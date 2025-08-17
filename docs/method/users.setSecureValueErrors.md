# users.setSecureValueErrors

**Description** : *Notify the user that the sent passport data contains some errors The user will not be able to re-submit their Passport data to you until the errors are fixed (the contents of the field for which you returned the error must change)*

**Layer** : 211

```tl
users.setSecureValueErrors#90c894b5 id:InputUser errors:Vector<SecureValueError> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>id</mark> | [`InputUser`](type/InputUser) | The user |
| <mark>errors</mark> | [`Vector<SecureValueError>`](type/SecureValueError) | Errors |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **USER_BOT_INVALID** | `403` | User accounts must provide the bot method parameter when calling this method. If there is no such method parameter, this method can only be invoked by bot accounts |
| **USER_BOT_REQUIRED** | `400` | This method can only be called by a bot |
| **USER_ID_INVALID** | `400` | The provided user ID is invalid |

---

## Example

```php
$bool = $client->users->setSecureValueErrors(
	id : $client->inputUserEmpty(),
	errors : array(
		$client->secureValueErrorData(
			type : $client->secureValueTypePersonalDetails(),
			data_hash : 'Κ??LiveProto???ϊ',
			field : 'wOmG2I9ErRxiZJH0',
			text : 't2lkzTYpXnomuC8B',
		),
		$client->secureValueErrorFrontSide(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : 't???LiveProto?\\?O',
			text : 'csxDOkWYunFA5twy',
		),
		$client->secureValueErrorReverseSide(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : '؜ LiveProto}???^',
			text : 'gsxpuLJVKHkWhj8d',
		),
		$client->secureValueErrorSelfie(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : '??.LiveProtoؖ??2',
			text : 'bVqyat4pdukSYZ61',
		),
		$client->secureValueErrorFile(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : '	?)AELiveProto???Z?',
			text : 'dlsOC85KxeRAVXar',
		),
		$client->secureValueErrorFiles(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : array('t?\'??LiveProto?L??'),
			text : 'PHnQtgBrd95ecRa1',
		),
		$client->secureValueError(
			type : $client->secureValueTypePersonalDetails(),
			hash : '?RSZ?LiveProto?=?',
			text : '31UYKwR9S6aDOcLA',
		),
		$client->secureValueErrorTranslationFile(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : '?r???LiveProto??ף',
			text : 'PQlcp9kGv7fOEiDm',
		),
		$client->secureValueErrorTranslationFiles(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : array('LQ' . "\0" . 'c?LiveProto??-??'),
			text : 'mdrsav4XZ6OtGISY',
		),
	),
);
```