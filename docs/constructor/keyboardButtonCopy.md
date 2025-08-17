# keyboardButtonCopy

**Description** : *Clipboard button: when clicked, the attached text must be copied to the clipboard*

**Layer** : 211

```tl
keyboardButtonCopy#75d2698e text:string copy_text:string = KeyboardButton;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>text</mark> | [`string`](type/string) | Title of the button |
| <mark>copy_text</mark> | [`string`](type/string) | The text that will be copied to the clipboard |

---

## Type

[KeyboardButton](type/KeyboardButton)

---

## Example

```php
$keyboardButton = $client->keyboardButtonCopy(
	text : 'lJ69SVniZN143YP0',
	copy_text : 'pJr9Lw72BigWHa6v',
);
```