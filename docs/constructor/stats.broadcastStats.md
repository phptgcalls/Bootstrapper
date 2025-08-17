# stats.broadcastStats

**Description** : *Channel statistics*

**Layer** : 211

```tl
stats.broadcastStats#396ca5fc period:StatsDateRangeDays followers:StatsAbsValueAndPrev views_per_post:StatsAbsValueAndPrev shares_per_post:StatsAbsValueAndPrev reactions_per_post:StatsAbsValueAndPrev views_per_story:StatsAbsValueAndPrev shares_per_story:StatsAbsValueAndPrev reactions_per_story:StatsAbsValueAndPrev enabled_notifications:StatsPercentValue growth_graph:StatsGraph followers_graph:StatsGraph mute_graph:StatsGraph top_hours_graph:StatsGraph interactions_graph:StatsGraph iv_interactions_graph:StatsGraph views_by_source_graph:StatsGraph new_followers_by_source_graph:StatsGraph languages_graph:StatsGraph reactions_by_emotion_graph:StatsGraph story_interactions_graph:StatsGraph story_reactions_by_emotion_graph:StatsGraph recent_posts_interactions:Vector<PostInteractionCounters> = stats.BroadcastStats;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>period</mark> | [`StatsDateRangeDays`](type/StatsDateRangeDays) | Period in consideration |
| <mark>followers</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | Follower count change for period in consideration |
| <mark>views_per_post</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | total_viewcount/postcount, for posts posted during the period in consideration. Note that in this case, current refers to the period in consideration (min_date till max_date), and prev refers to the previous period ((min_date - (max_date - min_date)) till min_date) |
| <mark>shares_per_post</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | total_sharecount/postcount, for posts posted during the period in consideration. Note that in this case, current refers to the period in consideration (min_date till max_date), and prev refers to the previous period ((min_date - (max_date - min_date)) till min_date) |
| <mark>reactions_per_post</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | total_reactions/postcount, for posts posted during the period in consideration. Note that in this case, current refers to the period in consideration (min_date till max_date), and prev refers to the previous period ((min_date - (max_date - min_date)) till min_date) |
| <mark>views_per_story</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | total_views/storycount, for posts posted during the period in consideration. Note that in this case, current refers to the period in consideration (min_date till max_date), and prev refers to the previous period ((min_date - (max_date - min_date)) till min_date) |
| <mark>shares_per_story</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | total_shares/storycount, for posts posted during the period in consideration. Note that in this case, current refers to the period in consideration (min_date till max_date), and prev refers to the previous period ((min_date - (max_date - min_date)) till min_date) |
| <mark>reactions_per_story</mark> | [`StatsAbsValueAndPrev`](type/StatsAbsValueAndPrev) | total_reactions/storycount, for posts posted during the period in consideration. Note that in this case, current refers to the period in consideration (min_date till max_date), and prev refers to the previous period ((min_date - (max_date - min_date)) till min_date) |
| <mark>enabled_notifications</mark> | [`StatsPercentValue`](type/StatsPercentValue) | Percentage of subscribers with enabled notifications |
| <mark>growth_graph</mark> | [`StatsGraph`](type/StatsGraph) | Channel growth graph (absolute subscriber count) |
| <mark>followers_graph</mark> | [`StatsGraph`](type/StatsGraph) | Followers growth graph (relative subscriber count) |
| <mark>mute_graph</mark> | [`StatsGraph`](type/StatsGraph) | Muted users graph (relative) |
| <mark>top_hours_graph</mark> | [`StatsGraph`](type/StatsGraph) | Views per hour graph (absolute) |
| <mark>interactions_graph</mark> | [`StatsGraph`](type/StatsGraph) | Interactions graph (absolute) |
| <mark>iv_interactions_graph</mark> | [`StatsGraph`](type/StatsGraph) | IV interactions graph (absolute) |
| <mark>views_by_source_graph</mark> | [`StatsGraph`](type/StatsGraph) | Views by source graph (absolute) |
| <mark>new_followers_by_source_graph</mark> | [`StatsGraph`](type/StatsGraph) | New followers by source graph (absolute) |
| <mark>languages_graph</mark> | [`StatsGraph`](type/StatsGraph) | Subscriber language graph (pie chart) |
| <mark>reactions_by_emotion_graph</mark> | [`StatsGraph`](type/StatsGraph) | A graph containing the number of reactions on posts categorized by emotion |
| <mark>story_interactions_graph</mark> | [`StatsGraph`](type/StatsGraph) | A graph containing the number of story views and shares |
| <mark>story_reactions_by_emotion_graph</mark> | [`StatsGraph`](type/StatsGraph) | A graph containing the number of reactions on stories categorized by emotion |
| <mark>recent_posts_interactions</mark> | [`Vector<PostInteractionCounters>`](type/PostInteractionCounters) | Detailed statistics about number of views and shares of recently sent messages and stories |

---

## Type

[stats.BroadcastStats](type/stats.BroadcastStats)

---

## Example

```php
$statsBroadcastStats = $client->stats->broadcastStats(
	period : $client->statsDateRangeDays(
		min_date : 74,
		max_date : 21,
	),
	followers : $client->statsAbsValueAndPrev(
		current : -1375175.03515625,
		previous : 1395263.3349609375,
	),
	views_per_post : $client->statsAbsValueAndPrev(
		current : -1838137.9404296875,
		previous : 1421953.0703125,
	),
	shares_per_post : $client->statsAbsValueAndPrev(
		current : -1916896.9091796875,
		previous : 2053301.4951171875,
	),
	reactions_per_post : $client->statsAbsValueAndPrev(
		current : 885600.306640625,
		previous : 1952348.8115234375,
	),
	views_per_story : $client->statsAbsValueAndPrev(
		current : 409370.4716796875,
		previous : -1404113.7177734375,
	),
	shares_per_story : $client->statsAbsValueAndPrev(
		current : -544499.513671875,
		previous : -42143.9931640625,
	),
	reactions_per_story : $client->statsAbsValueAndPrev(
		current : -612805.44140625,
		previous : -1477270.931640625,
	),
	enabled_notifications : $client->statsPercentValue(
		part : -1449431.978515625,
		total : -2029586.560546875,
	),
	growth_graph : $client->statsGraphAsync(
		token : 'p3JWaMnFP6GEVwvD',
	),
	followers_graph : $client->statsGraphAsync(
		token : 'WqCmeLPY62KgZVS5',
	),
	mute_graph : $client->statsGraphAsync(
		token : 'uxQsleFAHdi609Do',
	),
	top_hours_graph : $client->statsGraphAsync(
		token : 'hJVl6RWXcjvO1Ug4',
	),
	interactions_graph : $client->statsGraphAsync(
		token : 'rL5VaeADU8oXBs9t',
	),
	iv_interactions_graph : $client->statsGraphAsync(
		token : 'xfyt1SbaAEm2YUu6',
	),
	views_by_source_graph : $client->statsGraphAsync(
		token : 'Rs1jgSMnX34voPGU',
	),
	new_followers_by_source_graph : $client->statsGraphAsync(
		token : 'vbmCOqx1lnLZHgP4',
	),
	languages_graph : $client->statsGraphAsync(
		token : 'm4PVBfUecE1nxz32',
	),
	reactions_by_emotion_graph : $client->statsGraphAsync(
		token : 'NvjfWMGsRErSpaYt',
	),
	story_interactions_graph : $client->statsGraphAsync(
		token : 'Dig8BeQChqoO4j07',
	),
	story_reactions_by_emotion_graph : $client->statsGraphAsync(
		token : 'z3SDaXne8EpgUF4G',
	),
	recent_posts_interactions : array(
		$client->postInteractionCountersMessage(
			msg_id : 32,
			views : 38,
			forwards : 32,
			reactions : 35,
		),
		$client->postInteractionCountersStory(
			story_id : 94,
			views : 14,
			forwards : 30,
			reactions : 70,
		),
	),
);
```