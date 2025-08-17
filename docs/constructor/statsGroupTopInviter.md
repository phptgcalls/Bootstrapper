# statsGroupTopInviter

**Description** : *Information about an active supergroup inviter*

**Layer** : 211

```tl
statsGroupTopInviter#535f779d user_id:long invitations:int = StatsGroupTopInviter;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>user_id</mark> | [`long`](type/long) | User ID |
| <mark>invitations</mark> | [`int`](type/int) | Number of invitations for statistics period in consideration |

---

## Type

[StatsGroupTopInviter](type/StatsGroupTopInviter)

---

## Example

```php
$statsGroupTopInviter = $client->statsGroupTopInviter(
	user_id : 8917519419102898284,
	invitations : 82,
);
```