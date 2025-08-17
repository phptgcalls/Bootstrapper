# help.saveAppLog

**Description** : *Saves logs of application on the server*

**Layer** : 211

```tl
help.saveAppLog#6f02f748 events:Vector<InputAppEvent> = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>events</mark> | [`Vector<InputAppEvent>`](type/InputAppEvent) | List of input events |

---

## Result

[Bool](type/Bool)

---

## Example

```php
$bool = $client->help->saveAppLog(
	events : array(
		$client->inputAppEvent(
			time : -1532707.51171875,
			type : 'xlMZz2ucTJ5W4Q6y',
			peer : 7723706522658859045,
			data : $client->jsonNull(),
		),
	),
);
```