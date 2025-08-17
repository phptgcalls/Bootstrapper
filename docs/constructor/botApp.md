# botApp

**Description** : *Contains information about a direct link Mini App*

**Layer** : 211

```tl
botApp#95fcd1d6 flags:# id:long access_hash:long short_name:string title:string description:string photo:Photo document:flags.0?Document hash:long = BotApp;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>id</mark> | [`long`](type/long) | bot mini app ID |
| <mark>access_hash</mark> | [`long`](type/long) | bot mini app access hash |
| <mark>short_name</mark> | [`string`](type/string) | bot mini app short name, used to generate Direct Mini App deep links |
| <mark>title</mark> | [`string`](type/string) | bot mini app title |
| <mark>description</mark> | [`string`](type/string) | bot mini app description |
| <mark>photo</mark> | [`Photo`](type/Photo) | bot mini app photo |
| **document** | [`flags.0?Document`](type/Document) | bot mini app animation |
| <mark>hash</mark> | [`long`](type/long) | Hash to pass to messages.getBotApp, to avoid refetching bot app info if it hasn't changed |

---

## Type

[BotApp](type/BotApp)

---

## Example

```php
$botApp = $client->botApp(
	id : 2368050649322173732,
	access_hash : -8600511164968378142,
	short_name : 'ThDFglVrBOaIMd08',
	title : 'DVZIdA8YtOwPKB3M',
	description : 'P5LGsx7Y6p8Thlty',
	photo : $client->photoEmpty(
		id : 4083830034055127899,
	),
	document : $client->documentEmpty(
		id : -1037893754096565379,
	),
	hash : 2278601628077150873,
);
```