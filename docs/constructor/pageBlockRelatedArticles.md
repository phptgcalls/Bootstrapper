# pageBlockRelatedArticles

**Description** : *Related articles*

**Layer** : 211

```tl
pageBlockRelatedArticles#16115a96 title:RichText articles:Vector<PageRelatedArticle> = PageBlock;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>title</mark> | [`RichText`](type/RichText) | Title |
| <mark>articles</mark> | [`Vector<PageRelatedArticle>`](type/PageRelatedArticle) | Related articles |

---

## Type

[PageBlock](type/PageBlock)

---

## Example

```php
$pageBlock = $client->pageBlockRelatedArticles(
	title : $client->textEmpty(),
	articles : array(
		$client->pageRelatedArticle(
			url : 'https://docs.liveproto.dev',
			webpage_id : -5022257795067671496,
			title : 'E9gm0pkuT3lSeNOh',
			description : 'lYE6yqn47p5TMmAP',
			photo_id : -8420702577309024107,
			author : 'kytxnFXNfM9H1gqr',
			published_date : 15,
		),
	),
);
```