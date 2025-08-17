# pageBlockEmbed

**Description** : *An embedded webpage*

**Layer** : 211

```tl
pageBlockEmbed#a8718dc5 flags:# full_width:flags.0?true allow_scrolling:flags.3?true url:flags.1?string html:flags.2?string poster_photo_id:flags.4?long w:flags.5?int h:flags.5?int caption:PageCaption = PageBlock;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **full_width** | [`flags.0?true`](type/true) | Whether the block should be full width |
| **allow_scrolling** | [`flags.3?true`](type/true) | Whether scrolling should be allowed |
| **url** | [`flags.1?string`](type/string) | Web page URL, if available |
| **html** | [`flags.2?string`](type/string) | HTML-markup of the embedded page |
| **poster_photo_id** | [`flags.4?long`](type/long) | Poster photo, if available |
| **w** | [`flags.5?int`](type/int) | Block width, if known |
| **h** | [`flags.5?int`](type/int) | Block height, if known |
| <mark>caption</mark> | [`PageCaption`](type/PageCaption) | Caption |

---

## Type

[PageBlock](type/PageBlock)

---

## Example

```php
$pageBlock = $client->pageBlockEmbed(
	full_width : true,
	allow_scrolling : true,
	url : 'https://docs.liveproto.dev',
	html : 'hzWU1dtHTLODe6r4',
	poster_photo_id : 4597731154857550226,
	w : 76,
	h : 30,
	caption : $client->pageCaption(
		text : $client->textEmpty(),
		credit : $client->textEmpty(),
	),
);
```