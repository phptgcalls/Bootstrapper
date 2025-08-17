# textConcat

**Description** : *Concatenation of rich texts*

**Layer** : 211

```tl
textConcat#7e6260d7 texts:Vector<RichText> = RichText;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>texts</mark> | [`Vector<RichText>`](type/RichText) | Concatenated rich texts |

---

## Type

[RichText](type/RichText)

---

## Example

```php
$richText = $client->textConcat(
	texts : array(
		$client->textEmpty(),
		$client->textPlain(
			text : 'nFQduLzE2jog1R8A',
		),
		$client->textBold(
			text : $client->textEmpty(),
		),
		$client->textItalic(
			text : $client->textEmpty(),
		),
		$client->textUnderline(
			text : $client->textEmpty(),
		),
		$client->textStrike(
			text : $client->textEmpty(),
		),
		$client->textFixed(
			text : $client->textEmpty(),
		),
		$client->textUrl(
			text : $client->textEmpty(),
			url : 'https://docs.liveproto.dev',
			webpage_id : 7774689158207568545,
		),
		$client->textEmail(
			text : $client->textEmpty(),
			email : 'reply@liveproto.dev',
		),
		$client->textConcat(
			texts : array(
				$client->textEmpty(),
				$client->textPlain(
					text : 'h7rRpeLq4XYHCkwB',
				),
				$client->textBold(
					text : $client->textEmpty(...),
				),
				$client->textItalic(
					text : $client->textEmpty(...),
				),
				$client->textUnderline(
					text : $client->textEmpty(...),
				),
				$client->textStrike(
					text : $client->textEmpty(...),
				),
				$client->textFixed(
					text : $client->textEmpty(...),
				),
				$client->textUrl(
					text : $client->textEmpty(...),
					url : 'https://docs.liveproto.dev',
					webpage_id : -2686271260619484261,
				),
				$client->textEmail(
					text : $client->textEmpty(...),
					email : 'reply@liveproto.dev',
				),
				$client->textConcat(
					texts : array(
						$client->textEmpty(...),
						$client->textPlain(...),
						$client->textBold(...),
						$client->textItalic(...),
						$client->textUnderline(...),
						$client->textStrike(...),
						$client->textFixed(...),
						$client->textUrl(...),
						$client->textEmail(...),
						$client->textConcat(...),
						$client->textSubscript(...),
						$client->textSuperscript(...),
						$client->textMarked(...),
						$client->textPhone(...),
						$client->textImage(...),
						$client->textAnchor(...),
					),
				),
				$client->textSubscript(
					text : $client->textEmpty(...),
				),
				$client->textSuperscript(
					text : $client->textEmpty(...),
				),
				$client->textMarked(
					text : $client->textEmpty(...),
				),
				$client->textPhone(
					text : $client->textEmpty(...),
					phone : '+1234567890',
				),
				$client->textImage(
					document_id : 5858034373169172073,
					w : 12,
					h : 48,
				),
				$client->textAnchor(
					text : $client->textEmpty(...),
					name : 'nhd1cDeu9qHGaiwM',
				),
			),
		),
		$client->textSubscript(
			text : $client->textEmpty(),
		),
		$client->textSuperscript(
			text : $client->textEmpty(),
		),
		$client->textMarked(
			text : $client->textEmpty(),
		),
		$client->textPhone(
			text : $client->textEmpty(),
			phone : '+1234567890',
		),
		$client->textImage(
			document_id : 1048154422521828358,
			w : 14,
			h : 50,
		),
		$client->textAnchor(
			text : $client->textEmpty(),
			name : 'o5bGe9K4sdkIiUm0',
		),
	),
);
```