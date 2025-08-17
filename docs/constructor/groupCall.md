# groupCall

**Description** : *Info about a group call or livestream*

**Layer** : 211

```tl
groupCall#553b0ba1 flags:# join_muted:flags.1?true can_change_join_muted:flags.2?true join_date_asc:flags.6?true schedule_start_subscribed:flags.8?true can_start_video:flags.9?true record_video_active:flags.11?true rtmp_stream:flags.12?true listeners_hidden:flags.13?true conference:flags.14?true creator:flags.15?true id:long access_hash:long participants_count:int title:flags.3?string stream_dc_id:flags.4?int record_start_date:flags.5?int schedule_date:flags.7?int unmuted_video_count:flags.10?int unmuted_video_limit:int version:int invite_link:flags.16?string = GroupCall;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **join_muted** | [`flags.1?true`](type/true) | Whether the user should be muted upon joining the call |
| **can_change_join_muted** | [`flags.2?true`](type/true) | Whether the current user can change the value of the join_muted flag using phone.toggleGroupCallSettings |
| **join_date_asc** | [`flags.6?true`](type/true) | Specifies the ordering to use when locally sorting by date and displaying in the UI group call participants |
| **schedule_start_subscribed** | [`flags.8?true`](type/true) | Whether we subscribed to the scheduled call |
| **can_start_video** | [`flags.9?true`](type/true) | Whether you can start streaming video into the call |
| **record_video_active** | [`flags.11?true`](type/true) | Whether the group call is currently being recorded |
| **rtmp_stream** | [`flags.12?true`](type/true) | Whether RTMP streams are allowed |
| **listeners_hidden** | [`flags.13?true`](type/true) | Whether the listeners list is hidden and cannot be fetched using phone.getGroupParticipants. The phone.groupParticipants.count and groupCall.participants_count counters will still include listeners |
| **conference** | [`flags.14?true`](type/true) | NOTHING |
| **creator** | [`flags.15?true`](type/true) | NOTHING |
| <mark>id</mark> | [`long`](type/long) | Group call ID |
| <mark>access_hash</mark> | [`long`](type/long) | Group call access hash |
| <mark>participants_count</mark> | [`int`](type/int) | Participant count |
| **title** | [`flags.3?string`](type/string) | Group call title |
| **stream_dc_id** | [`flags.4?int`](type/int) | DC ID to be used for livestream chunks |
| **record_start_date** | [`flags.5?int`](type/int) | When was the recording started |
| **schedule_date** | [`flags.7?int`](type/int) | When is the call scheduled to start |
| **unmuted_video_count** | [`flags.10?int`](type/int) | Number of people currently streaming video into the call |
| <mark>unmuted_video_limit</mark> | [`int`](type/int) | Maximum number of people allowed to stream video into the call |
| <mark>version</mark> | [`int`](type/int) | Version |
| **invite_link** | [`flags.16?string`](type/string) | NOTHING |

---

## Type

[GroupCall](type/GroupCall)

---

## Example

```php
$groupCall = $client->groupCall(
	join_muted : true,
	can_change_join_muted : true,
	join_date_asc : true,
	schedule_start_subscribed : true,
	can_start_video : true,
	record_video_active : true,
	rtmp_stream : true,
	listeners_hidden : true,
	conference : true,
	creator : true,
	id : 4664964805525289471,
	access_hash : -2441759367945418630,
	participants_count : 98,
	title : 'QqVkrN4vLy2EBdi7',
	stream_dc_id : 98,
	record_start_date : 14,
	schedule_date : 87,
	unmuted_video_count : 91,
	unmuted_video_limit : 100,
	version : 60,
	invite_link : 'hYE3lCSixk5oBHNA',
);
```