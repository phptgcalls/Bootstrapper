# pollAnswerVoters

**Description** : *A poll answer, and how users voted on it*

**Layer** : 211

```tl
pollAnswerVoters#3b6ddad2 flags:# chosen:flags.0?true correct:flags.1?true option:bytes voters:int = PollAnswerVoters;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **chosen** | [`flags.0?true`](type/true) | Whether we have chosen this answer |
| **correct** | [`flags.1?true`](type/true) | For quizzes, whether the option we have chosen is correct |
| <mark>option</mark> | [`bytes`](type/bytes) | The param that has to be passed to messages.sendVote |
| <mark>voters</mark> | [`int`](type/int) | How many users voted for this option |

---

## Type

[PollAnswerVoters](type/PollAnswerVoters)

---

## Example

```php
$pollAnswerVoters = $client->pollAnswerVoters(
	chosen : true,
	correct : true,
	option : ']?p?LiveProto??AL',
	voters : 87,
);
```