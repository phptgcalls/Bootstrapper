# pageBlockOrderedList

**Description** : *Ordered list of IV blocks*

**Layer** : 211

```tl
pageBlockOrderedList#9a8ae1e1 items:Vector<PageListOrderedItem> = PageBlock;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>items</mark> | [`Vector<PageListOrderedItem>`](type/PageListOrderedItem) | List items |

---

## Type

[PageBlock](type/PageBlock)

---

## Example

```php
$pageBlock = $client->pageBlockOrderedList(
	items : array(
		$client->pageListOrderedItemText(
			num : 'oiQKe1j5p9L6YZGA',
			text : $client->textEmpty(),
		),
		$client->pageListOrderedItemBlocks(
			num : 'tY5s9gnCVFP8KevL',
			blocks : array(
				$client->pageBlockUnsupported(),
				$client->pageBlockTitle(
					text : $client->textEmpty(...),
				),
				$client->pageBlockSubtitle(
					text : $client->textEmpty(...),
				),
				$client->pageBlockAuthorDate(
					author : $client->textEmpty(...),
					published_date : 99,
				),
				$client->pageBlockHeader(
					text : $client->textEmpty(...),
				),
				$client->pageBlockSubheader(
					text : $client->textEmpty(...),
				),
				$client->pageBlockParagraph(
					text : $client->textEmpty(...),
				),
				$client->pageBlockPreformatted(
					text : $client->textEmpty(...),
					language : 'XMzPgOhv0q3oYr6b',
				),
				$client->pageBlockFooter(
					text : $client->textEmpty(...),
				),
				$client->pageBlockDivider(),
				$client->pageBlockAnchor(
					name : 'qnLX69t8FMycGR5E',
				),
				$client->pageBlockList(
					items : array(
						$client->pageListItemText(...),
						$client->pageListItemBlocks(...),
					),
				),
				$client->pageBlockBlockquote(
					text : $client->textEmpty(...),
					caption : $client->textEmpty(...),
				),
				$client->pageBlockPullquote(
					text : $client->textEmpty(...),
					caption : $client->textEmpty(...),
				),
				$client->pageBlockPhoto(
					photo_id : 8637314445910517011,
					caption : $client->pageCaption(...),
					url : 'https://docs.liveproto.dev',
					webpage_id : 7770043873260299326,
				),
				$client->pageBlockVideo(
					autoplay : true,
					loop : true,
					video_id : 9191521353906202341,
					caption : $client->pageCaption(...),
				),
				$client->pageBlockCover(
					cover : $client->pageBlockUnsupported(...),
				),
				$client->pageBlockEmbed(
					full_width : true,
					allow_scrolling : true,
					url : 'https://docs.liveproto.dev',
					html : 'O6TiVdcu3CjeLSU2',
					poster_photo_id : -4304653973919731638,
					w : 9,
					h : 0,
					caption : $client->pageCaption(...),
				),
				$client->pageBlockEmbedPost(
					url : 'https://docs.liveproto.dev',
					webpage_id : -3065361917051618967,
					author_photo_id : 7313508697781343073,
					author : 'AxCUmYpQaERqN5ZX',
					date : 85,
					blocks : array(
						$client->pageBlockUnsupported(...),
						$client->pageBlockTitle(...),
						$client->pageBlockSubtitle(...),
						$client->pageBlockAuthorDate(...),
						$client->pageBlockHeader(...),
						$client->pageBlockSubheader(...),
						$client->pageBlockParagraph(...),
						$client->pageBlockPreformatted(...),
						$client->pageBlockFooter(...),
						$client->pageBlockDivider(...),
						$client->pageBlockAnchor(...),
						$client->pageBlockList(...),
						$client->pageBlockBlockquote(...),
						$client->pageBlockPullquote(...),
						$client->pageBlockPhoto(...),
						$client->pageBlockVideo(...),
						$client->pageBlockCover(...),
						$client->pageBlockEmbed(...),
						$client->pageBlockEmbedPost(...),
						$client->pageBlockCollage(...),
						$client->pageBlockSlideshow(...),
						$client->pageBlockChannel(...),
						$client->pageBlockAudio(...),
						$client->pageBlockKicker(...),
						$client->pageBlockTable(...),
						$client->pageBlockOrderedList(...),
						$client->pageBlockDetails(...),
						$client->pageBlockRelatedArticles(...),
						$client->pageBlockMap(...),
					),
					caption : $client->pageCaption(...),
				),
				$client->pageBlockCollage(
					items : array(
						$client->pageBlockUnsupported(...),
						$client->pageBlockTitle(...),
						$client->pageBlockSubtitle(...),
						$client->pageBlockAuthorDate(...),
						$client->pageBlockHeader(...),
						$client->pageBlockSubheader(...),
						$client->pageBlockParagraph(...),
						$client->pageBlockPreformatted(...),
						$client->pageBlockFooter(...),
						$client->pageBlockDivider(...),
						$client->pageBlockAnchor(...),
						$client->pageBlockList(...),
						$client->pageBlockBlockquote(...),
						$client->pageBlockPullquote(...),
						$client->pageBlockPhoto(...),
						$client->pageBlockVideo(...),
						$client->pageBlockCover(...),
						$client->pageBlockEmbed(...),
						$client->pageBlockEmbedPost(...),
						$client->pageBlockCollage(...),
						$client->pageBlockSlideshow(...),
						$client->pageBlockChannel(...),
						$client->pageBlockAudio(...),
						$client->pageBlockKicker(...),
						$client->pageBlockTable(...),
						$client->pageBlockOrderedList(...),
						$client->pageBlockDetails(...),
						$client->pageBlockRelatedArticles(...),
						$client->pageBlockMap(...),
					),
					caption : $client->pageCaption(...),
				),
				$client->pageBlockSlideshow(
					items : array(
						$client->pageBlockUnsupported(...),
						$client->pageBlockTitle(...),
						$client->pageBlockSubtitle(...),
						$client->pageBlockAuthorDate(...),
						$client->pageBlockHeader(...),
						$client->pageBlockSubheader(...),
						$client->pageBlockParagraph(...),
						$client->pageBlockPreformatted(...),
						$client->pageBlockFooter(...),
						$client->pageBlockDivider(...),
						$client->pageBlockAnchor(...),
						$client->pageBlockList(...),
						$client->pageBlockBlockquote(...),
						$client->pageBlockPullquote(...),
						$client->pageBlockPhoto(...),
						$client->pageBlockVideo(...),
						$client->pageBlockCover(...),
						$client->pageBlockEmbed(...),
						$client->pageBlockEmbedPost(...),
						$client->pageBlockCollage(...),
						$client->pageBlockSlideshow(...),
						$client->pageBlockChannel(...),
						$client->pageBlockAudio(...),
						$client->pageBlockKicker(...),
						$client->pageBlockTable(...),
						$client->pageBlockOrderedList(...),
						$client->pageBlockDetails(...),
						$client->pageBlockRelatedArticles(...),
						$client->pageBlockMap(...),
					),
					caption : $client->pageCaption(...),
				),
				$client->pageBlockChannel(
					channel : $client->chatEmpty(...),
				),
				$client->pageBlockAudio(
					audio_id : -2022937258935831984,
					caption : $client->pageCaption(...),
				),
				$client->pageBlockKicker(
					text : $client->textEmpty(...),
				),
				$client->pageBlockTable(
					bordered : true,
					striped : true,
					title : $client->textEmpty(...),
					rows : array(
						$client->pageTableRow(...),
					),
				),
				$client->pageBlockOrderedList(
					items : array(
						$client->pageListOrderedItemText(...),
						$client->pageListOrderedItemBlocks(...),
					),
				),
				$client->pageBlockDetails(
					open : true,
					blocks : array(
						$client->pageBlockUnsupported(...),
						$client->pageBlockTitle(...),
						$client->pageBlockSubtitle(...),
						$client->pageBlockAuthorDate(...),
						$client->pageBlockHeader(...),
						$client->pageBlockSubheader(...),
						$client->pageBlockParagraph(...),
						$client->pageBlockPreformatted(...),
						$client->pageBlockFooter(...),
						$client->pageBlockDivider(...),
						$client->pageBlockAnchor(...),
						$client->pageBlockList(...),
						$client->pageBlockBlockquote(...),
						$client->pageBlockPullquote(...),
						$client->pageBlockPhoto(...),
						$client->pageBlockVideo(...),
						$client->pageBlockCover(...),
						$client->pageBlockEmbed(...),
						$client->pageBlockEmbedPost(...),
						$client->pageBlockCollage(...),
						$client->pageBlockSlideshow(...),
						$client->pageBlockChannel(...),
						$client->pageBlockAudio(...),
						$client->pageBlockKicker(...),
						$client->pageBlockTable(...),
						$client->pageBlockOrderedList(...),
						$client->pageBlockDetails(...),
						$client->pageBlockRelatedArticles(...),
						$client->pageBlockMap(...),
					),
					title : $client->textEmpty(...),
				),
				$client->pageBlockRelatedArticles(
					title : $client->textEmpty(...),
					articles : array(
						$client->pageRelatedArticle(...),
					),
				),
				$client->pageBlockMap(
					geo : $client->geoPointEmpty(...),
					zoom : 64,
					w : 53,
					h : 16,
					caption : $client->pageCaption(...),
				),
			),
		),
	),
);
```