# updateGroupCallParticipants

**Description** : *The participant list of a certain group call has changed*

**Layer** : 211

```tl
updateGroupCallParticipants#f2ebdb4e call:InputGroupCall participants:Vector<GroupCallParticipant> version:int = Update;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>call</mark> | [`InputGroupCall`](type/InputGroupCall) | Group call |
| <mark>participants</mark> | [`Vector<GroupCallParticipant>`](type/GroupCallParticipant) | New participant list |
| <mark>version</mark> | [`int`](type/int) | Version |

---

## Type

[Update](type/Update)

---

## Example

```php
$update = $client->updateGroupCallParticipants(
	call : $client->inputGroupCall(
		id : -1901172589382364991,
		access_hash : 4106137352083626895,
	),
	participants : array(
		$client->groupCallParticipant(
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
				user_id : -9100926487770363944,
			),
			date : 70,
			active_date : 41,
			source : 62,
			volume : 27,
			about : 'B350NVyHl4eghkL8',
			raise_hand_rating : -368911703515165179,
			video : $client->groupCallParticipantVideo(
				paused : true,
				endpoint : '49eCA82dFup7DcYy',
				source_groups : array(
					$client->groupCallParticipantVideoSourceGroup(...),
				),
				audio_source : 16,
			),
			presentation : $client->groupCallParticipantVideo(
				paused : true,
				endpoint : 'wxvK5oTzZtcU2C1Y',
				source_groups : array(
					$client->groupCallParticipantVideoSourceGroup(...),
				),
				audio_source : 0,
			),
		),
	),
	version : 66,
);
```