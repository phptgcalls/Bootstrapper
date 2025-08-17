# keyboardButtonRow

**Description** : *Inline keyboard row*

**Layer** : 211

```tl
keyboardButtonRow#77608b83 buttons:Vector<KeyboardButton> = KeyboardButtonRow;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>buttons</mark> | [`Vector<KeyboardButton>`](type/KeyboardButton) | Bot or inline keyboard buttons |

---

## Type

[KeyboardButtonRow](type/KeyboardButtonRow)

---

## Example

```php
$keyboardButtonRow = $client->keyboardButtonRow(
	buttons : array(
		$client->keyboardButton(
			text : 'kfq6ApCtHLF3KR2z',
		),
		$client->keyboardButtonUrl(
			text : 'pyd0oTYblChGZQc9',
			url : 'https://docs.liveproto.dev',
		),
		$client->keyboardButtonCallback(
			requires_password : true,
			text : 'whqnx62FGIzoR0Z9',
			data : '?????LiveProtoo?(?~',
		),
		$client->keyboardButtonRequestPhone(
			text : 'D7LBa5gRbF4hcsxe',
		),
		$client->keyboardButtonRequestGeoLocation(
			text : 'ZOeYt8F7BciA0Hhy',
		),
		$client->keyboardButtonSwitchInline(
			same_peer : true,
			text : '8VdcMqD9P1ysQvxW',
			query : 'uY3J7dScIkwVCbsE',
			peer_types : array(
				$client->inlineQueryPeerTypeSameBotPM(),
				$client->inlineQueryPeerTypePM(),
				$client->inlineQueryPeerTypeChat(),
				$client->inlineQueryPeerTypeMegagroup(),
				$client->inlineQueryPeerTypeBroadcast(),
				$client->inlineQueryPeerTypeBotPM(),
			),
		),
		$client->keyboardButtonGame(
			text : '8h02VPYvwUK4XFZS',
		),
		$client->keyboardButtonBuy(
			text : 'jrS9To36v1thzluL',
		),
		$client->keyboardButtonUrlAuth(
			text : 'sYnod5ePyOIMmXLD',
			fwd_text : '2DUmWqF6LZwkSBGf',
			url : 'https://docs.liveproto.dev',
			button_id : 61,
		),
		$client->inputKeyboardButtonUrlAuth(
			request_write_access : true,
			text : 'uUejqyY4HfCksznm',
			fwd_text : 'krVuAYD2wWgJnF8q',
			url : 'https://docs.liveproto.dev',
			bot : $client->inputUserEmpty(),
		),
		$client->keyboardButtonRequestPoll(
			quiz : $client->boolFalse(),
			text : 'vmZX14jPNifyAsJw',
		),
		$client->inputKeyboardButtonUserProfile(
			text : 'rvz2DH7Tkq4QMWpA',
			user_id : $client->inputUserEmpty(),
		),
		$client->keyboardButtonUserProfile(
			text : 'UzkV8iQfd9vgPhIE',
			user_id : 8310365718441515207,
		),
		$client->keyboardButtonWebView(
			text : 'KfCwe8trzSo4pWQg',
			url : 'https://docs.liveproto.dev',
		),
		$client->keyboardButtonSimpleWebView(
			text : 'KjRsubQ8pN6BUEAT',
			url : 'https://docs.liveproto.dev',
		),
		$client->keyboardButtonRequestPeer(
			text : '9NkTFCaUpWKJswMO',
			button_id : 79,
			peer_type : $client->requestPeerTypeUser(
				bot : $client->boolFalse(...),
				premium : $client->boolFalse(...),
			),
			max_quantity : 47,
		),
		$client->inputKeyboardButtonRequestPeer(
			name_requested : true,
			username_requested : true,
			photo_requested : true,
			text : 'SiwYEFlPXVecMup8',
			button_id : 66,
			peer_type : $client->requestPeerTypeUser(
				bot : $client->boolFalse(...),
				premium : $client->boolFalse(...),
			),
			max_quantity : 4,
		),
		$client->keyboardButtonCopy(
			text : 'xw69LsEO5rhnjAIH',
			copy_text : 'gAsrH1mY5CjdeXVJ',
		),
	),
);
```