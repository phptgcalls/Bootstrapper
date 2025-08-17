# keyboardButtonSimpleWebView

**Description** : *Button to open a bot mini app using messages.requestSimpleWebView, without sending user information to the web app*

**Layer** : 211

```tl
keyboardButtonSimpleWebView#a0c0505c text:string url:string = KeyboardButton;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>text</mark> | [`string`](type/string) | Button text |
| <mark>url</mark> | [`string`](type/string) | Web app URL |

---

## Type

[KeyboardButton](type/KeyboardButton)

---

## Example

```php
$keyboardButton = $client->keyboardButtonSimpleWebView(
	text : 'LBQ3wycSxsztDE19',
	url : 'https://docs.liveproto.dev',
);
```