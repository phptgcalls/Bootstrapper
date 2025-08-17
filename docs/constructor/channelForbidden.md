# channelForbidden

**Description** : *Indicates a channel/supergroup we can't access because we were banned, or for some other reason*

**Layer** : 211

```tl
channelForbidden#17d493d5 flags:# broadcast:flags.5?true megagroup:flags.8?true id:long access_hash:long title:string until_date:flags.16?int = Chat;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **broadcast** | [`flags.5?true`](type/true) | Is this a channel |
| **megagroup** | [`flags.8?true`](type/true) | Is this a supergroup |
| <mark>id</mark> | [`long`](type/long) | Channel ID |
| <mark>access_hash</mark> | [`long`](type/long) | Access hash |
| <mark>title</mark> | [`string`](type/string) | Title |
| **until_date** | [`flags.16?int`](type/int) | The ban is valid until the specified date |

---

## Type

[Chat](type/Chat)

---

## Example

```php
$chat = $client->channelForbidden(
	broadcast : true,
	megagroup : true,
	id : -9170815983280697364,
	access_hash : -2658514814388040757,
	title : 'eRvxQLyl426qGdPK',
	until_date : 74,
);
```