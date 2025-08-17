# updateBotWebhookJSON

**Description** : *A new incoming event; for bots only*

**Layer** : 211

```tl
updateBotWebhookJSON#8317c0c3 data:DataJSON = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>data</mark> | [`DataJSON`](type/DataJSON) | The event |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateBotWebhookJSON(
	data : $client->dataJSON(
		data : 'gDqBdjZAarzo1hMt',
	),
);
```