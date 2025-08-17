# highScore

**Description** : *Game highscore*

**Layer** : 211

```tl
highScore#73a379eb pos:int user_id:long score:int = HighScore;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>pos</mark> | [`int`](type/int) | Position in highscore list |
| <mark>user_id</mark> | [`long`](type/long) | User ID |
| <mark>score</mark> | [`int`](type/int) | Score |

---

## Type

[HighScore](type/HighScore)

---

## Example

```php
$highScore = $client->highScore(
	pos : 34,
	user_id : 1753974205822396866,
	score : 89,
);
```