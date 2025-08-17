# KeyboardButton

**Description** : *Bot or inline keyboard buttons*

**Layer** : 211

```tl
keyboardButton#a2fa4880 text:string = KeyboardButton;
keyboardButtonUrl#258aff05 text:string url:string = KeyboardButton;
keyboardButtonCallback#35bbdb6b flags:# requires_password:flags.0?true text:string data:bytes = KeyboardButton;
keyboardButtonRequestPhone#b16a6c29 text:string = KeyboardButton;
keyboardButtonRequestGeoLocation#fc796b3f text:string = KeyboardButton;
keyboardButtonSwitchInline#93b9fbb5 flags:# same_peer:flags.0?true text:string query:string peer_types:flags.1?Vector<InlineQueryPeerType> = KeyboardButton;
keyboardButtonGame#50f41ccf text:string = KeyboardButton;
keyboardButtonBuy#afd93fbb text:string = KeyboardButton;
keyboardButtonUrlAuth#10b78d29 flags:# text:string fwd_text:flags.0?string url:string button_id:int = KeyboardButton;
inputKeyboardButtonUrlAuth#d02e7fd4 flags:# request_write_access:flags.0?true text:string fwd_text:flags.1?string url:string bot:InputUser = KeyboardButton;
keyboardButtonRequestPoll#bbc7515d flags:# quiz:flags.0?Bool text:string = KeyboardButton;
inputKeyboardButtonUserProfile#e988037b text:string user_id:InputUser = KeyboardButton;
keyboardButtonUserProfile#308660c1 text:string user_id:long = KeyboardButton;
keyboardButtonWebView#13767230 text:string url:string = KeyboardButton;
keyboardButtonSimpleWebView#a0c0505c text:string url:string = KeyboardButton;
keyboardButtonRequestPeer#53d7bfd8 text:string button_id:int peer_type:RequestPeerType max_quantity:int = KeyboardButton;
inputKeyboardButtonRequestPeer#c9662d05 flags:# name_requested:flags.0?true username_requested:flags.1?true photo_requested:flags.2?true text:string button_id:int peer_type:RequestPeerType max_quantity:int = KeyboardButton;
keyboardButtonCopy#75d2698e text:string copy_text:string = KeyboardButton;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**keyboardButton**](constructor/keyboardButton) | Bot keyboard button |
| [**keyboardButtonUrl**](constructor/keyboardButtonUrl) | URL button |
| [**keyboardButtonCallback**](constructor/keyboardButtonCallback) | Callback button |
| [**keyboardButtonRequestPhone**](constructor/keyboardButtonRequestPhone) | Button to request a user's phone number |
| [**keyboardButtonRequestGeoLocation**](constructor/keyboardButtonRequestGeoLocation) | Button to request a user's geolocation |
| [**keyboardButtonSwitchInline**](constructor/keyboardButtonSwitchInline) | Button to force a user to switch to inline mode: pressing the button will prompt the user to select one of their chats, open that chat and insert the bot's username and the specified inline query in the input field |
| [**keyboardButtonGame**](constructor/keyboardButtonGame) | Button to start a game |
| [**keyboardButtonBuy**](constructor/keyboardButtonBuy) | Button to buy a product |
| [**keyboardButtonUrlAuth**](constructor/keyboardButtonUrlAuth) | Button to request a user to authorize via URL using Seamless Telegram Login. When the user clicks on such a button, messages.requestUrlAuth should be called, providing the button_id and the ID of the container message. The returned urlAuthResultRequest object will contain more details about the authorization request (request_write_access if the bot would like to send messages to the user along with the username of the bot which will be used for user authorization). Finally, the user can choose to call messages.acceptUrlAuth to get a urlAuthResultAccepted with the URL to open instead of the url of this constructor, or a urlAuthResultDefault, in which case the url of this constructor must be opened, instead. If the user refuses the authorization request but still wants to open the link, the url of this constructor must be used |
| [**inputKeyboardButtonUrlAuth**](constructor/inputKeyboardButtonUrlAuth) | Button to request a user to authorize via URL using Seamless Telegram Login |
| [**keyboardButtonRequestPoll**](constructor/keyboardButtonRequestPoll) | A button that allows the user to create and send a poll when pressed; available only in private |
| [**inputKeyboardButtonUserProfile**](constructor/inputKeyboardButtonUserProfile) | Button that links directly to a user profile |
| [**keyboardButtonUserProfile**](constructor/keyboardButtonUserProfile) | Button that links directly to a user profile |
| [**keyboardButtonWebView**](constructor/keyboardButtonWebView) | Button to open a bot mini app using messages.requestWebView, sending over user information after user confirmation.Can only be sent or received as part of an inline keyboard, use keyboardButtonSimpleWebView for reply keyboards |
| [**keyboardButtonSimpleWebView**](constructor/keyboardButtonSimpleWebView) | Button to open a bot mini app using messages.requestSimpleWebView, without sending user information to the web app.Can only be sent or received as part of a reply keyboard, use keyboardButtonWebView for inline keyboards |
| [**keyboardButtonRequestPeer**](constructor/keyboardButtonRequestPeer) | Prompts the user to select and share one or more peers with the bot using messages.sendBotRequestedPeer |
| [**inputKeyboardButtonRequestPeer**](constructor/inputKeyboardButtonRequestPeer) | Prompts the user to select and share one or more peers with the bot using messages.sendBotRequestedPeer |
| [**keyboardButtonCopy**](constructor/keyboardButtonCopy) | Clipboard button: when clicked, the attached text must be copied to the clipboard |