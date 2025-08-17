# messageMediaGame

**Description** : *Telegram game*

**Layer** : 211

```tl
messageMediaGame#fdb19008 game:Game = MessageMedia;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>game</mark> | [`Game`](type/Game) | Game |

---

## Type

[MessageMedia](type/MessageMedia)

---

## Example

```php
$messageMedia = $client->messageMediaGame(
	game : $client->game(
		id : 3693116066829799707,
		access_hash : -5501893846804477330,
		short_name : 'vH3CwI2aq0UyPW79',
		title : 'D87Qm6KxOoFZkPyR',
		description : 'aKv8gD9OkVFuzSxR',
		photo : $client->photoEmpty(
			id : 3733469913580196405,
		),
		document : $client->documentEmpty(
			id : -1010433565433736773,
		),
	),
);
```