# sponsoredMessageReportOption

**Description** : *A report option for a sponsored message »*

**Layer** : 211

```tl
sponsoredMessageReportOption#430d3150 text:string option:bytes = SponsoredMessageReportOption;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>text</mark> | [`string`](type/string) | Localized description of the option |
| <mark>option</mark> | [`bytes`](type/bytes) | Option identifier to pass to channels.reportSponsoredMessage |

---

## Type

[SponsoredMessageReportOption](type/SponsoredMessageReportOption)

---

## Example

```php
$sponsoredMessageReportOption = $client->sponsoredMessageReportOption(
	text : '9qMtSVXj4D5euKAo',
	option : '???<LiveProto4^??t',
);
```