# jsonArray

**Description** : *JSON array*

**Layer** : 211

```tl
jsonArray#f7444763 value:Vector<JSONValue> = JSONValue;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>value</mark> | [`Vector<JSONValue>`](type/JSONValue) | JSON values |

---

## Type

[JSONValue](type/JSONValue)

---

## Example

```php
$jSONValue = $client->jsonArray(
	value : array(
		$client->jsonNull(),
		$client->jsonBool(
			value : $client->boolFalse(),
		),
		$client->jsonNumber(
			value : 607169.55078125,
		),
		$client->jsonString(
			value : 'v9VWAP1JZ2NtreTq',
		),
		$client->jsonArray(
			value : array(
				$client->jsonNull(),
				$client->jsonBool(
					value : $client->boolFalse(...),
				),
				$client->jsonNumber(
					value : -313824.5029296875,
				),
				$client->jsonString(
					value : 'GuJdaneUP4tAwzsI',
				),
				$client->jsonArray(
					value : array(
						$client->jsonNull(...),
						$client->jsonBool(...),
						$client->jsonNumber(...),
						$client->jsonString(...),
						$client->jsonArray(...),
						$client->jsonObject(...),
					),
				),
				$client->jsonObject(
					value : array(
						$client->jsonObjectValue(...),
					),
				),
			),
		),
		$client->jsonObject(
			value : array(
				$client->jsonObjectValue(
					key : '1JZMQonNFhbXPTLC',
					value : $client->jsonNull(...),
				),
			),
		),
	),
);
```