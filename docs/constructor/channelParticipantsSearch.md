# channelParticipantsSearch

**Description** : *Query participants by name*

**Layer** : 211

```tl
channelParticipantsSearch#656ac4b q:string = ChannelParticipantsFilter;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>q</mark> | [`string`](type/string) | Search query |

---

## Type

[ChannelParticipantsFilter](type/ChannelParticipantsFilter)

---

## Example

```php
$channelParticipantsFilter = $client->channelParticipantsSearch(
	q : 'OkG3coN9CX0hqdQa',
);
```