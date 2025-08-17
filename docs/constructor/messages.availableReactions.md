# messages.availableReactions

**Description** : *Animations and metadata associated with message reactions »*

**Layer** : 211

```tl
messages.availableReactions#768e3aad hash:int reactions:Vector<AvailableReaction> = messages.AvailableReactions;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>hash</mark> | [`int`](type/int) | Hash used for caching, for more info click here |
| <mark>reactions</mark> | [`Vector<AvailableReaction>`](type/AvailableReaction) | Animations and metadata associated with message reactions » |

---

## Type

[messages.AvailableReactions](type/messages.AvailableReactions)

---

## Example

```php
$messagesAvailableReactions = $client->messages->availableReactions(
	hash : 37,
	reactions : array(
		$client->availableReaction(
			inactive : true,
			premium : true,
			reaction : 'T5SUQD4PbjYGMV9F',
			title : 'sOCYF2MiTeuQnyc1',
			static_icon : $client->documentEmpty(
				id : 8230515379328398558,
			),
			appear_animation : $client->documentEmpty(
				id : 7113881126544921052,
			),
			select_animation : $client->documentEmpty(
				id : 900294862063490202,
			),
			activate_animation : $client->documentEmpty(
				id : 6683431108958958190,
			),
			effect_animation : $client->documentEmpty(
				id : -3138889510968650659,
			),
			around_animation : $client->documentEmpty(
				id : -4584207288299536850,
			),
			center_icon : $client->documentEmpty(
				id : 3175225124888416708,
			),
		),
	),
);
```