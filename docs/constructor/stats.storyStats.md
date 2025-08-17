# stats.storyStats

**Description** : *Contains statistics about a story*

**Layer** : 211

```tl
stats.storyStats#50cd067c views_graph:StatsGraph reactions_by_emotion_graph:StatsGraph = stats.StoryStats;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>views_graph</mark> | [`StatsGraph`](type/StatsGraph) | A graph containing the number of story views and shares |
| <mark>reactions_by_emotion_graph</mark> | [`StatsGraph`](type/StatsGraph) | A bar graph containing the number of story reactions categorized by "emotion" (i.e. Positive, Negative, Other, etc...) |

---

## Type

[stats.StoryStats](type/stats.StoryStats)

---

## Example

```php
$statsStoryStats = $client->stats->storyStats(
	views_graph : $client->statsGraphAsync(
		token : 's7kwCIQFKx6aeuO8',
	),
	reactions_by_emotion_graph : $client->statsGraphAsync(
		token : 'bn20ZKkc9hRWym4e',
	),
);
```