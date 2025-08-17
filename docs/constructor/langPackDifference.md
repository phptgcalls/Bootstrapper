# langPackDifference

**Description** : *Changes to the app's localization pack*

**Layer** : 211

```tl
langPackDifference#f385c1f6 lang_code:string from_version:int version:int strings:Vector<LangPackString> = LangPackDifference;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>lang_code</mark> | [`string`](type/string) | Language code |
| <mark>from_version</mark> | [`int`](type/int) | Previous version number |
| <mark>version</mark> | [`int`](type/int) | New version number |
| <mark>strings</mark> | [`Vector<LangPackString>`](type/LangPackString) | Localized strings |

---

## Type

[LangPackDifference](type/LangPackDifference)

---

## Example

```php
$langPackDifference = $client->langPackDifference(
	lang_code : '8GgqyQpSwEHhrFVW',
	from_version : 84,
	version : 65,
	strings : array(
		$client->langPackString(
			key : 'eOT7uPUMdohysi0x',
			value : 'prP6Fez4EIqXGyub',
		),
		$client->langPackStringPluralized(
			key : 'PjkR8gUcBGNO7sY0',
			zero_value : 'cXhd5xQUEbposTu2',
			one_value : 'eDigKXR6BWhaTlQZ',
			two_value : 'arRC4nAgZ6XY1uy9',
			few_value : 'UaqoLVCuX76mGr8g',
			many_value : 'kzygWrYcsx8M4R02',
			other_value : 'GeKkV37L2HIuAoEt',
		),
		$client->langPackStringDeleted(
			key : 'pWMUBTX5A1PdOQkw',
		),
	),
);
```