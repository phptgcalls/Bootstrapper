# stories.searchPosts

**Description** : *Globally search for stories using a hashtag or a location media area, see here » for more info on the full flow*

**Layer** : 211

```tl
stories.searchPosts#d1810907 flags:# hashtag:flags.0?string area:flags.1?MediaArea peer:flags.2?InputPeer offset:string limit:int = stories.FoundStories;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **hashtag** | [`flags.0?string`](type/string) | Hashtag (without the #) |
| **area** | [`flags.1?MediaArea`](type/MediaArea) | A mediaAreaGeoPoint or a mediaAreaVenue.  Note mediaAreaGeoPoint areas may be searched only if they have an associated address |
| **peer** | [`flags.2?InputPeer`](type/InputPeer) | If set, returns only stories posted by this peer |
| <mark>offset</mark> | [`string`](type/string) | Offset for pagination: initially an empty string, then the next_offset from the previously returned stories.foundStories |
| <mark>limit</mark> | [`int`](type/int) | Maximum number of results to return, see pagination |

---

## Result

[stories.FoundStories](type/stories.FoundStories)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **HASHTAG_INVALID** | `400` | The specified hashtag is invalid |

---

## Example

```php
$storiesFoundStories = $client->stories->searchPosts(
	hashtag : 'BPTkSa6ef3WsMgVp',
	area : $client->mediaAreaVenue(
		coordinates : $client->mediaAreaCoordinates(
			x : 89978.294921875,
			y : 518063.5205078125,
			w : -799841.1982421875,
			h : -1094524.0849609375,
			rotation : -1930550.498046875,
			radius : 2001702.7802734375,
		),
		geo : $client->geoPointEmpty(),
		title : 'OSLhV2cjY8TRIsuz',
		address : '9gBmOH2uyvQUIz3n',
		provider : 'OvR5XLltNeyGCA1r',
		venue_id : 'lbgnZsyHrS4mJdvQ',
		venue_type : 'I5Nxj9YTZnaOK3gl',
	),
	peer : $client->inputPeerEmpty(),
	offset : 'RlpxvGWf0TCjoiq2',
	limit : 70,
);
```