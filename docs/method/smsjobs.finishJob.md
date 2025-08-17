# smsjobs.finishJob

**Description** : *Finish an SMS job (official clients only)*

**Layer** : 211

```tl
smsjobs.finishJob#4f1ebf24 flags:# job_id:string error:flags.0?string = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| <mark>job_id</mark> | [`string`](type/string) | Job ID |
| **error** | [`flags.0?string`](type/string) | If failed, the error |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **SMSJOB_ID_INVALID** | `400` | The specified job ID is invalid |

---

## Example

```php
$bool = $client->smsjobs->finishJob(
	job_id : 'Puf2j7oz6pwDOqIa',
	error : 'j2PF71COaLiZf0hN',
);
```