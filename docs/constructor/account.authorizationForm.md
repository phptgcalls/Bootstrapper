# account.authorizationForm

**Description** : *Telegram Passport authorization form*

**Layer** : 211

```tl
account.authorizationForm#ad2e1cd8 flags:# required_types:Vector<SecureRequiredType> values:Vector<SecureValue> errors:Vector<SecureValueError> users:Vector<User> privacy_policy_url:flags.0?string = account.AuthorizationForm;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>required_types</mark> | [`Vector<SecureRequiredType>`](type/SecureRequiredType) | Required Telegram Passport documents |
| <mark>values</mark> | [`Vector<SecureValue>`](type/SecureValue) | Already submitted Telegram Passport documents |
| <mark>errors</mark> | [`Vector<SecureValueError>`](type/SecureValueError) | Telegram Passport errors |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about the bot to which the form will be submitted |
| **privacy_policy_url** | [`flags.0?string`](type/string) | URL of the service's privacy policy |

---

## Type

[account.AuthorizationForm](type/account.AuthorizationForm)

---

## Example

```php
$accountAuthorizationForm = $client->account->authorizationForm(
	required_types : array(
		$client->secureRequiredType(
			native_names : true,
			selfie_required : true,
			translation_required : true,
			type : $client->secureValueTypePersonalDetails(),
		),
		$client->secureRequiredTypeOneOf(
			types : array(
				$client->secureRequiredType(
					native_names : true,
					selfie_required : true,
					translation_required : true,
					type : $client->secureValueTypePersonalDetails(...),
				),
				$client->secureRequiredTypeOneOf(
					types : array(
						$client->secureRequiredType(...),
						$client->secureRequiredTypeOneOf(...),
					),
				),
			),
		),
	),
	values : array(
		$client->secureValue(
			type : $client->secureValueTypePersonalDetails(),
			data : $client->secureData(
				data : '.)??LiveProto?`?f?',
				data_hash : '`??KoLiveProto?????',
				secret : 'M?c?LiveProtoF{U?',
			),
			front_side : $client->secureFileEmpty(),
			reverse_side : $client->secureFileEmpty(),
			selfie : $client->secureFileEmpty(),
			translation : array(
				$client->secureFileEmpty(),
				$client->secureFile(
					id : 6626532206748725066,
					access_hash : -8060400444742551183,
					size : -2730367273217023888,
					dc_id : 51,
					date : 73,
					file_hash : '?????LiveProto???',
					secret : '??C?LiveProto?X?',
				),
			),
			files : array(
				$client->secureFileEmpty(),
				$client->secureFile(
					id : -6292842219614820296,
					access_hash : 2864770777879272354,
					size : -5764494491180067444,
					dc_id : 44,
					date : 38,
					file_hash : '??	܆LiveProto?h
Y?',
					secret : 'lMޫ?LiveProto?uV?',
				),
			),
			plain_data : $client->securePlainPhone(
				phone : '+1234567890',
			),
			hash : '88???LiveProto?>i??',
		),
	),
	errors : array(
		$client->secureValueErrorData(
			type : $client->secureValueTypePersonalDetails(),
			data_hash : '*???LiveProto;ʵ?',
			field : 'QrC5WRI2hEXKY93t',
			text : 'iPU6AhmeloT4FjbO',
		),
		$client->secureValueErrorFrontSide(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : ':???LiveProtopAԾm',
			text : 'wdWGrot827g94ZbN',
		),
		$client->secureValueErrorReverseSide(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : '.?@uLiveProto%Ӽ{',
			text : 'GYHJrKe5cWoRxOjV',
		),
		$client->secureValueErrorSelfie(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : '	??g<LiveProtoE??y|',
			text : 'JSqyhEMHuZ43U1GB',
		),
		$client->secureValueErrorFile(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : 'l?Np?LiveProto?)???',
			text : 'q2LimZrOwFaBeTV1',
		),
		$client->secureValueErrorFiles(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : array('b9bLiveProto???y'),
			text : 'nRubt0Jkd4zLraog',
		),
		$client->secureValueError(
			type : $client->secureValueTypePersonalDetails(),
			hash : '\\?-[.LiveProtof?Q??',
			text : 'skM9TV7dUKnPZyCR',
		),
		$client->secureValueErrorTranslationFile(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : 'XT?#=LiveProto>8',
			text : 'DfqgvnpMQzGZYrco',
		),
		$client->secureValueErrorTranslationFiles(
			type : $client->secureValueTypePersonalDetails(),
			file_hash : array('?,?LiveProtobɰ?_'),
			text : 'EYjQA3NgPIqXa56H',
		),
	),
	users : array(
		$client->userEmpty(
			id : -4695179596516390940,
		),
		$client->user(
			self : true,
			contact : true,
			mutual_contact : true,
			deleted : true,
			bot : true,
			bot_chat_history : true,
			bot_nochats : true,
			verified : true,
			restricted : true,
			min : true,
			bot_inline_geo : true,
			support : true,
			scam : true,
			apply_min_photo : true,
			fake : true,
			bot_attach_menu : true,
			premium : true,
			attach_menu_enabled : true,
			bot_can_edit : true,
			close_friend : true,
			stories_hidden : true,
			stories_unavailable : true,
			contact_require_premium : true,
			bot_business : true,
			bot_has_main_app : true,
			id : -8618078295820299952,
			access_hash : 4850104400616118540,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 25,
			restriction_reason : array(
				$client->restrictionReason(
					platform : '9hT0Dxj8k3Bz2aXQ',
					reason : 'xSKs7Za8DVjnfBb6',
					text : 'xLm1sG25eATZ0NtW',
				),
			),
			bot_inline_placeholder : 'sFS8XJdBa0V3Pv4K',
			lang_code : 'gdjMnX4WSfzyBer6',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 48,
			color : $client->peerColor(
				color : 78,
				background_emoji_id : 5020615631745939876,
			),
			profile_color : $client->peerColor(
				color : 41,
				background_emoji_id : 8204278493871862267,
			),
			bot_active_users : 82,
			bot_verification_icon : 6134851132573564866,
			send_paid_messages_stars : 912413286816958187,
		),
	),
	privacy_policy_url : 'https://docs.liveproto.dev',
);
```