# channelAdminLogEventActionParticipantMute

**Description** : *A group call participant was muted*

**Layer** : 211

```tl
channelAdminLogEventActionParticipantMute#f92424d2 participant:GroupCallParticipant = ChannelAdminLogEventAction;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>participant</mark> | [`GroupCallParticipant`](type/GroupCallParticipant) | The participant that was muted |

---

## Type

[ChannelAdminLogEventAction](type/ChannelAdminLogEventAction)

---

## Example

```php
$channelAdminLogEventAction = $client->channelAdminLogEventActionParticipantMute(
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
			user_id : 3541743855973327055,
		),
		date : 7,
		active_date : 25,
		source : 26,
		volume : 97,
		about : '6ZrDPBdxioCW1L0s',
		raise_hand_rating : -290641496497048401,
		video : $client->groupCallParticipantVideo(
			paused : true,
			endpoint : 'IyEVTDiOqvhQou8Y',
			source_groups : array(
				$client->groupCallParticipantVideoSourceGroup(...),
			),
			audio_source : 77,
		),
		presentation : $client->groupCallParticipantVideo(
			paused : true,
			endpoint : '3msNLKOXPBlZ98rM',
			source_groups : array(
				$client->groupCallParticipantVideoSourceGroup(...),
			),
			audio_source : 65,
		),
	),
);
```