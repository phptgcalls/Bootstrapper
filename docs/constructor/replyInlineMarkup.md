# replyInlineMarkup

**Description** : *Bot or inline keyboard*

**Layer** : 211

```tl
replyInlineMarkup#48a30254 rows:Vector<KeyboardButtonRow> = ReplyMarkup;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>rows</mark> | [`Vector<KeyboardButtonRow>`](type/KeyboardButtonRow) | Bot or inline keyboard rows |

---

## Type

[ReplyMarkup](type/ReplyMarkup)

---

## Example

```php
$replyMarkup = $client->replyInlineMarkup(
	rows : array(
		$client->keyboardButtonRow(
			buttons : array(
				$client->keyboardButton(
					text : '5dA6lB8nxoZvweiV',
				),
				$client->keyboardButtonUrl(
					text : 'uwDnIrHvWURfOplS',
					url : 'https://docs.liveproto.dev',
				),
				$client->keyboardButtonCallback(
					requires_password : true,
					text : 'MbDlgnUdIyhqrNvj',
					data : '?' . "\0" . 'Y?pLiveProto+e??U',
				),
				$client->keyboardButtonRequestPhone(
					text : 'XT4g29huG3yJFrcH',
				),
				$client->keyboardButtonRequestGeoLocation(
					text : 'T0VYPOobBa6qFsdw',
				),
				$client->keyboardButtonSwitchInline(
					same_peer : true,
					text : 'vVYa4xGNUfkPdzq9',
					query : 'gGyXHq0DiaMAYzCS',
					peer_types : array(
						$client->inlineQueryPeerTypeSameBotPM(...),
						$client->inlineQueryPeerTypePM(...),
						$client->inlineQueryPeerTypeChat(...),
						$client->inlineQueryPeerTypeMegagroup(...),
						$client->inlineQueryPeerTypeBroadcast(...),
						$client->inlineQueryPeerTypeBotPM(...),
					),
				),
				$client->keyboardButtonGame(
					text : 'hgv4xYjDZOTJf1LF',
				),
				$client->keyboardButtonBuy(
					text : 'PwA1KXiFYb2IR5aE',
				),
				$client->keyboardButtonUrlAuth(
					text : 'PCbps3aMdi6OGWe1',
					fwd_text : 'OmVpoBLPv82EZkdn',
					url : 'https://docs.liveproto.dev',
					button_id : 40,
				),
				$client->inputKeyboardButtonUrlAuth(
					request_write_access : true,
					text : 'VDULixpzkPeotFKW',
					fwd_text : 'aVGLuWKvcxyp4fBo',
					url : 'https://docs.liveproto.dev',
					bot : $client->inputUserEmpty(...),
				),
				$client->keyboardButtonRequestPoll(
					quiz : $client->boolFalse(...),
					text : 'UnuaVQKmZ4SbjFIp',
				),
				$client->inputKeyboardButtonUserProfile(
					text : '9obsOyKuWwHQPapU',
					user_id : $client->inputUserEmpty(...),
				),
				$client->keyboardButtonUserProfile(
					text : '9WjC1aOnh5w7kiZx',
					user_id : 7714075631799914105,
				),
				$client->keyboardButtonWebView(
					text : 'srZ2vERMHm9WlyJT',
					url : 'https://docs.liveproto.dev',
				),
				$client->keyboardButtonSimpleWebView(
					text : 'bxItYM4GfTnFwyPg',
					url : 'https://docs.liveproto.dev',
				),
				$client->keyboardButtonRequestPeer(
					text : 'QrTEXJ9q2iI4FmH6',
					button_id : 39,
					peer_type : $client->requestPeerTypeUser(...),
					max_quantity : 33,
				),
				$client->inputKeyboardButtonRequestPeer(
					name_requested : true,
					username_requested : true,
					photo_requested : true,
					text : 'XML6IH8ceExfCA01',
					button_id : 43,
					peer_type : $client->requestPeerTypeUser(...),
					max_quantity : 26,
				),
				$client->keyboardButtonCopy(
					text : 'ADMVyg8Wj7Eb34T0',
					copy_text : '5096nKqAHr8yk3UZ',
				),
			),
		),
	),
);
```