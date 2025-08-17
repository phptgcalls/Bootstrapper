# replyKeyboardMarkup

**Description** : *Bot keyboard*

**Layer** : 211

```tl
replyKeyboardMarkup#85dd99d1 flags:# resize:flags.0?true single_use:flags.1?true selective:flags.2?true persistent:flags.4?true rows:Vector<KeyboardButtonRow> placeholder:flags.3?string = ReplyMarkup;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **resize** | [`flags.0?true`](type/true) | Requests clients to resize the keyboard vertically for optimal fit (e.g., make the keyboard smaller if there are just two rows of buttons). If not set, the custom keyboard is always of the same height as the app's standard keyboard |
| **single_use** | [`flags.1?true`](type/true) | Requests clients to hide the keyboard as soon as it's been used. The keyboard will still be available, but clients will automatically display the usual letter-keyboard in the chat – the user can press a special button in the input field to see the custom keyboard again |
| **selective** | [`flags.2?true`](type/true) | Use this parameter if you want to show the keyboard to specific users only. Targets: 1) users that are @mentioned in the text of the Message object; 2) if the bot's message is a reply (has reply_to_message_id), sender of the original message.Example: A user requests to change the bot's language, bot replies to the request with a keyboard to select the new language. Other users in the group don't see the keyboard |
| **persistent** | [`flags.4?true`](type/true) | Requests clients to always show the keyboard when the regular keyboard is hidden |
| <mark>rows</mark> | [`Vector<KeyboardButtonRow>`](type/KeyboardButtonRow) | Button row |
| **placeholder** | [`flags.3?string`](type/string) | The placeholder to be shown in the input field when the keyboard is active; 1-64 characters |

---

## Type

[ReplyMarkup](type/ReplyMarkup)

---

## Example

```php
$replyMarkup = $client->replyKeyboardMarkup(
	resize : true,
	single_use : true,
	selective : true,
	persistent : true,
	rows : array(
		$client->keyboardButtonRow(
			buttons : array(
				$client->keyboardButton(
					text : 'bk2Qq8ydsRfClrPg',
				),
				$client->keyboardButtonUrl(
					text : 'YbGcr5ma3txnkKu9',
					url : 'https://docs.liveproto.dev',
				),
				$client->keyboardButtonCallback(
					requires_password : true,
					text : 'PhDdR9E5fVsbni62',
					data : '??@3@LiveProto???',
				),
				$client->keyboardButtonRequestPhone(
					text : 'MYOArE7ycxm2sCZ4',
				),
				$client->keyboardButtonRequestGeoLocation(
					text : 'hgTPc4lis0GOL8ZK',
				),
				$client->keyboardButtonSwitchInline(
					same_peer : true,
					text : 'i4Qf9hd6Mw0kFDbE',
					query : 'QuN4hFHSj1ORTy7t',
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
					text : 'FYkVscwOmfTdgzA4',
				),
				$client->keyboardButtonBuy(
					text : 'fbiXl7xAwJnK2P4Y',
				),
				$client->keyboardButtonUrlAuth(
					text : 'AfJ9jgwCKbRO5Ex3',
					fwd_text : 'JkHvMlCNE3umcwQs',
					url : 'https://docs.liveproto.dev',
					button_id : 25,
				),
				$client->inputKeyboardButtonUrlAuth(
					request_write_access : true,
					text : 'MKiUuo6P9HVmThSC',
					fwd_text : 'yFeuJ4V9jopY7bOw',
					url : 'https://docs.liveproto.dev',
					bot : $client->inputUserEmpty(...),
				),
				$client->keyboardButtonRequestPoll(
					quiz : $client->boolFalse(...),
					text : 'NvHQPOFerJcnlw0s',
				),
				$client->inputKeyboardButtonUserProfile(
					text : '9ECB5HxbvNIYhGPa',
					user_id : $client->inputUserEmpty(...),
				),
				$client->keyboardButtonUserProfile(
					text : 'kX0JchjwW7ft5R6O',
					user_id : -3387875514197011486,
				),
				$client->keyboardButtonWebView(
					text : 'yPJgoZb6Q7q83v2K',
					url : 'https://docs.liveproto.dev',
				),
				$client->keyboardButtonSimpleWebView(
					text : 'x7pwDWJ0dIYMBhuZ',
					url : 'https://docs.liveproto.dev',
				),
				$client->keyboardButtonRequestPeer(
					text : 'G0laNMkFU5PjQdLp',
					button_id : 27,
					peer_type : $client->requestPeerTypeUser(...),
					max_quantity : 33,
				),
				$client->inputKeyboardButtonRequestPeer(
					name_requested : true,
					username_requested : true,
					photo_requested : true,
					text : 'JdswNGgUAe19KRXY',
					button_id : 35,
					peer_type : $client->requestPeerTypeUser(...),
					max_quantity : 38,
				),
				$client->keyboardButtonCopy(
					text : 'ABS179FTOyQfCljU',
					copy_text : 'oRiCgYBbOPFvpE43',
				),
			),
		),
	),
	placeholder : 'REpfHjxgZm4P3GMQ',
);
```