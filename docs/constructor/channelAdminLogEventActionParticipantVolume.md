# channelAdminLogEventActionParticipantVolume

**Description** : *channelAdminLogEvent.user_id has set the volume of participant.peer to participant.volume*

**Layer** : 211

```tl
channelAdminLogEventActionParticipantVolume#3e7f6847 participant:GroupCallParticipant = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>participant</mark> | [`GroupCallParticipant`](type/GroupCallParticipant) | The participant whose volume was changed |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionParticipantVolume(
	participant : $client->groupCallParticipant(
		muted : true,
		left : true,
		can_self_unmute : true,
		just_joined : true,
		versioned : true,
		min : true,
		muted_by_you : true,
		volume_by_admin : true,
		self : true,
		video_joined : true,
		peer : $client->peerUser(
			user_id : 1436573828869308058,
		),
		date : 46,
		active_date : 23,
		source : 69,
		volume : 53,
		about : 'xJ2crOGqnPeWgDXF',
		raise_hand_rating : 748813316539477930,
		video : $client->groupCallParticipantVideo(
			paused : true,
			endpoint : 'CnfSgcARXvhHI2o5',
			source_groups : array(
				$client->groupCallParticipantVideoSourceGroup(...),
			),
			audio_source : 16,
		),
		presentation : $client->groupCallParticipantVideo(
			paused : true,
			endpoint : 'JoRdYGxPgEWcAjIt',
			source_groups : array(
				$client->groupCallParticipantVideoSourceGroup(...),
			),
			audio_source : 60,
		),
	),
);
```