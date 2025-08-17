# stats.megagroupStats

**Description** : *Supergroup statistics*

**Layer** : 211

```tl
stats.megagroupStats#ef7ff916 period:StatsDateRangeDays members:StatsAbsValueAndPrev messages:StatsAbsValueAndPrev viewers:StatsAbsValueAndPrev posters:StatsAbsValueAndPrev growth_graph:StatsGraph members_graph:StatsGraph new_members_by_source_graph:StatsGraph languages_graph:StatsGraph messages_graph:StatsGraph actions_graph:StatsGraph top_hours_graph:StatsGraph weekdays_graph:StatsGraph top_posters:Vector<StatsGroupTopPoster> top_admins:Vector<StatsGroupTopAdmin> top_inviters:Vector<StatsGroupTopInviter> users:Vector<User> = stats.MegagroupStats;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>period</mark> | [`StatsDateRangeDays`](type/StatsDateRangeDays) | Period in consideration |
| <mark>members</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | Member count change for period in consideration |
| <mark>messages</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | Message number change for period in consideration |
| <mark>viewers</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | Number of users that viewed messages, for range in consideration |
| <mark>posters</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | Number of users that posted messages, for range in consideration |
| <mark>growth_graph</mark> | [`StatsGraph`](type/StatsGraph) | Supergroup growth graph (absolute subscriber count) |
| <mark>members_graph</mark> | [`StatsGraph`](type/StatsGraph) | Members growth (relative subscriber count) |
| <mark>new_members_by_source_graph</mark> | [`StatsGraph`](type/StatsGraph) | New members by source graph |
| <mark>languages_graph</mark> | [`StatsGraph`](type/StatsGraph) | Subscriber language graph (pie chart) |
| <mark>messages_graph</mark> | [`StatsGraph`](type/StatsGraph) | Message activity graph (stacked bar graph, message type) |
| <mark>actions_graph</mark> | [`StatsGraph`](type/StatsGraph) | Group activity graph (deleted, modified messages, blocked users) |
| <mark>top_hours_graph</mark> | [`StatsGraph`](type/StatsGraph) | Activity per hour graph (absolute) |
| <mark>weekdays_graph</mark> | [`StatsGraph`](type/StatsGraph) | Activity per day of week graph (absolute) |
| <mark>top_posters</mark> | [`Vector<StatsGroupTopPoster>`](type/StatsGroupTopPoster) | Info about most active group members |
| <mark>top_admins</mark> | [`Vector<StatsGroupTopAdmin>`](type/StatsGroupTopAdmin) | Info about most active group admins |
| <mark>top_inviters</mark> | [`Vector<StatsGroupTopInviter>`](type/StatsGroupTopInviter) | Info about most active group inviters |
| <mark>users</mark> | [`Vector<User>`](type/User) | Info about users mentioned in statistics |

---

## Type

[stats.MegagroupStats](type/stats.MegagroupStats)

---

## Example

```php
$statsMegagroupStats = $client->stats->megagroupStats(
	period : $client->statsDateRangeDays(
		min_date : 44,
		max_date : 27,
	),
	members : $client->statsAbsValueAndPrev(
		current : 389670.37109375,
		previous : -2095990.7294921875,
	),
	messages : $client->statsAbsValueAndPrev(
		current : -1482082.8544921875,
		previous : -554982.4501953125,
	),
	viewers : $client->statsAbsValueAndPrev(
		current : -1400476.025390625,
		previous : -218608.048828125,
	),
	posters : $client->statsAbsValueAndPrev(
		current : 689392.8388671875,
		previous : -754327.390625,
	),
	growth_graph : $client->statsGraphAsync(
		token : 'yvRiao120A97UwZ6',
	),
	members_graph : $client->statsGraphAsync(
		token : 'A9m1elVa6ZETnU8r',
	),
	new_members_by_source_graph : $client->statsGraphAsync(
		token : 'BSCY8RsN30WP5ZqF',
	),
	languages_graph : $client->statsGraphAsync(
		token : '0F4KZIodqQEDRifv',
	),
	messages_graph : $client->statsGraphAsync(
		token : 'i3O6KDHQnM94oG7p',
	),
	actions_graph : $client->statsGraphAsync(
		token : 'Qv8NV4rFRTLadxSX',
	),
	top_hours_graph : $client->statsGraphAsync(
		token : '5lFAU47WhGEXgMPf',
	),
	weekdays_graph : $client->statsGraphAsync(
		token : 'zSNw0Zb45c8xyeJj',
	),
	top_posters : array(
		$client->statsGroupTopPoster(
			user_id : -4891677573289957094,
			messages : 84,
			avg_chars : 73,
		),
	),
	top_admins : array(
		$client->statsGroupTopAdmin(
			user_id : 9206763920589338731,
			deleted : 58,
			kicked : 81,
			banned : 1,
		),
	),
	top_inviters : array(
		$client->statsGroupTopInviter(
			user_id : -4225393660012617764,
			invitations : 69,
		),
	),
	users : array(
		$client->userEmpty(
			id : 8485355039279080923,
		),
		$client->user(
			self : true,
			contact : true,
			mutual_contact : true,
			deleted : true,
			bot : true,
			bot_chat_history : true,
			bot_nochats : true,
			verified : true,
			restricted : true,
			min : true,
			bot_inline_geo : true,
			support : true,
			scam : true,
			apply_min_photo : true,
			fake : true,
			bot_attach_menu : true,
			premium : true,
			attach_menu_enabled : true,
			bot_can_edit : true,
			close_friend : true,
			stories_hidden : true,
			stories_unavailable : true,
			contact_require_premium : true,
			bot_business : true,
			bot_has_main_app : true,
			id : -5516026681651554916,
			access_hash : 1428205135433628610,
			first_name : 'Tak',
			last_name : 'None',
			username : 'TakNone',
			phone : '+1234567890',
			photo : $client->userProfilePhotoEmpty(),
			status : $client->userStatusEmpty(),
			bot_info_version : 31,
			restriction_reason : array(
				$client->restrictionReason(
					platform : 'E4obqQB9vyD8fsew',
					reason : 'ybCk5Efz87ZMqPrx',
					text : 'rIVziq1mpScHbgjE',
				),
			),
			bot_inline_placeholder : 'jXBZRTyDWQK1aY8h',
			lang_code : 'bZ83X0haNVtEcUxj',
			emoji_status : $client->emojiStatusEmpty(),
			usernames : array(
				$client->username(
					editable : true,
					active : true,
					username : 'TakNone',
				),
			),
			stories_max_id : 43,
			color : $client->peerColor(
				color : 61,
				background_emoji_id : -5125875866384398160,
			),
			profile_color : $client->peerColor(
				color : 75,
				background_emoji_id : -7733579324125068303,
			),
			bot_active_users : 13,
			bot_verification_icon : 753714120842814770,
			send_paid_messages_stars : -2917500941824556000,
		),
	),
);
```