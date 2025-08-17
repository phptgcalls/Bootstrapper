# reportResultChooseOption

**Description** : *The user must choose one of the following options, and then messages.report must be re-invoked, passing the option's option identifier to messages.report.option*

**Layer** : 211

```tl
reportResultChooseOption#f0e4e0b6 title:string options:Vector<MessageReportOption> = ReportResult;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>title</mark> | [`string`](type/string) | Title of the option popup |
| <mark>options</mark> | [`Vector<MessageReportOption>`](type/MessageReportOption) | Available options, rendered as menu entries |

---

## Type

[ReportResult](type/ReportResult)

---

## Example

```php
$reportResult = $client->reportResultChooseOption(
	title : 'rlmot7juFxVJNkQf',
	options : array(
		$client->messageReportOption(
			text : 'w0d64mRuDHBGZXYM',
			option : '???R?LiveProtoVfw?',
		),
	),
);
```