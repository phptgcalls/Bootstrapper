# webPage

**Description** : *Webpage preview*

**Layer** : 211

```tl
webPage#e89c45b2 flags:# has_large_media:flags.13?true video_cover_photo:flags.14?true id:long url:string display_url:string hash:int type:flags.0?string site_name:flags.1?string title:flags.2?string description:flags.3?string photo:flags.4?Photo embed_url:flags.5?string embed_type:flags.5?string embed_width:flags.6?int embed_height:flags.6?int duration:flags.7?int author:flags.8?string document:flags.9?Document cached_page:flags.10?Page attributes:flags.12?Vector<WebPageAttribute> = WebPage;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>flags</mark> | [`#`](type/#) | Flags, see TL conditional fields |
| **has_large_media** | [`flags.13?true`](type/true) | Whether the size of the media in the preview can be changed |
| **video_cover_photo** | [`flags.14?true`](type/true) | NOTHING |
| <mark>id</mark> | [`long`](type/long) | Preview ID |
| <mark>url</mark> | [`string`](type/string) | URL of previewed webpage |
| <mark>display_url</mark> | [`string`](type/string) | Webpage URL to be displayed to the user |
| <mark>hash</mark> | [`int`](type/int) | Hash used for caching, for more info click here |
| **type** | [`flags.0?string`](type/string) | Type of the web page. One of the following: - video- gif- photo- document- profile- telegram_background- telegram_theme- telegram_story- telegram_channel- telegram_channel_request- telegram_megagroup- telegram_chat- telegram_megagroup_request- telegram_chat_request- telegram_album- telegram_message- telegram_bot- telegram_voicechat- telegram_livestream- telegram_user- telegram_botapp- telegram_channel_boost- telegram_group_boost- telegram_giftcode- telegram_stickerset |
| **site_name** | [`flags.1?string`](type/string) | Short name of the site (e.g., Google Docs, App Store) |
| **title** | [`flags.2?string`](type/string) | Title of the content |
| **description** | [`flags.3?string`](type/string) | Content description |
| **photo** | [`flags.4?Photo`](type/Photo) | Image representing the content |
| **embed_url** | [`flags.5?string`](type/string) | URL to show in the embedded preview |
| **embed_type** | [`flags.5?string`](type/string) | MIME type of the embedded preview, (e.g., text/html or video/mp4) |
| **embed_width** | [`flags.6?int`](type/int) | Width of the embedded preview |
| **embed_height** | [`flags.6?int`](type/int) | Height of the embedded preview |
| **duration** | [`flags.7?int`](type/int) | Duration of the content, in seconds |
| **author** | [`flags.8?string`](type/string) | Author of the content |
| **document** | [`flags.9?Document`](type/Document) | Preview of the content as a media file |
| **cached_page** | [`flags.10?Page`](type/Page) | Page contents in instant view format |
| **attributes** | [`flags.12?Vector<WebPageAttribute>`](type/WebPageAttribute) | Webpage attributes |

---

## Type

[WebPage](type/WebPage)

---

## Example

```php
$webPage = $client->webPage(
	has_large_media : true,
	video_cover_photo : true,
	id : 3736204400237051817,
	url : 'https://docs.liveproto.dev',
	display_url : 'https://docs.liveproto.dev',
	hash : 40,
	type : 'kXqptd9GvLyEIgaD',
	site_name : '24IGrOYXnQFktldv',
	title : 'lJoTYPvpcKgxMNRj',
	description : 'eik5Tv9qjXuoNf1M',
	photo : $client->photoEmpty(
		id : -7277787664715085839,
	),
	embed_url : 'https://docs.liveproto.dev',
	embed_type : 'azd70j1QEGtWh6Pg',
	embed_width : 2,
	embed_height : 38,
	duration : 94,
	author : 'PKNX7wpaU1QI6ROJ',
	document : $client->documentEmpty(
		id : -2071001368595495169,
	),
	cached_page : $client->page(
		part : true,
		rtl : true,
		v2 : true,
		url : 'https://docs.liveproto.dev',
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
				published_date : 50,
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
				language : 'UJY68OBwIsKAuDWd',
			),
			$client->pageBlockFooter(
				text : $client->textEmpty(...),
			),
			$client->pageBlockDivider(),
			$client->pageBlockAnchor(
				name : 'GstT9RB2NMnYDi1e',
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
				photo_id : -2504079356213634467,
				caption : $client->pageCaption(...),
				url : 'https://docs.liveproto.dev',
				webpage_id : 8238738715514055257,
			),
			$client->pageBlockVideo(
				autoplay : true,
				loop : true,
				video_id : -3388040436680128870,
				caption : $client->pageCaption(...),
			),
			$client->pageBlockCover(
				cover : $client->pageBlockUnsupported(...),
			),
			$client->pageBlockEmbed(
				full_width : true,
				allow_scrolling : true,
				url : 'https://docs.liveproto.dev',
				html : 'iWsflBq5nEDuLpdN',
				poster_photo_id : -11891752915742410,
				w : 12,
				h : 33,
				caption : $client->pageCaption(...),
			),
			$client->pageBlockEmbedPost(
				url : 'https://docs.liveproto.dev',
				webpage_id : -3936573395088213256,
				author_photo_id : -3133731168330720697,
				author : 'GWnktPSQMOyJodDi',
				date : 70,
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
				audio_id : -2551963610503209109,
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
				zoom : 28,
				w : 51,
				h : 88,
				caption : $client->pageCaption(...),
			),
		),
		photos : array(
			$client->photoEmpty(
				id : 7944129073190116048,
			),
			$client->photo(
				has_stickers : true,
				id : 2425086660750971369,
				access_hash : 8292287012368577212,
				file_reference : '.1/LiveProto?2jt?',
				date : 37,
				sizes : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				video_sizes : array(
					$client->videoSize(...),
					$client->videoSizeEmojiMarkup(...),
					$client->videoSizeStickerMarkup(...),
				),
				dc_id : 25,
			),
		),
		documents : array(
			$client->documentEmpty(
				id : 7394491570976811944,
			),
			$client->document(
				id : -5767767707769831268,
				access_hash : -6989521042449940700,
				file_reference : 'cQ??LiveProto?	?1;',
				date : 17,
				mime_type : 'FLl2NTmj04518DI3',
				size : -1262054610111236880,
				thumbs : array(
					$client->photoSizeEmpty(...),
					$client->photoSize(...),
					$client->photoCachedSize(...),
					$client->photoStrippedSize(...),
					$client->photoSizeProgressive(...),
					$client->photoPathSize(...),
				),
				video_thumbs : array(
					$client->videoSize(...),
					$client->videoSizeEmojiMarkup(...),
					$client->videoSizeStickerMarkup(...),
				),
				dc_id : 16,
				attributes : array(
					$client->documentAttributeImageSize(...),
					$client->documentAttributeAnimated(...),
					$client->documentAttributeSticker(...),
					$client->documentAttributeVideo(...),
					$client->documentAttributeAudio(...),
					$client->documentAttributeFilename(...),
					$client->documentAttributeHasStickers(...),
					$client->documentAttributeCustomEmoji(...),
				),
			),
		),
		views : 77,
	),
	attributes : array(
		$client->webPageAttributeTheme(
			documents : array(
				$client->documentEmpty(
					id : 785014695063778718,
				),
				$client->document(
					id : 196718160294017460,
					access_hash : 506710308389171467,
					file_reference : '?I?N?LiveProto3aN?',
					date : 54,
					mime_type : 'W0b5huMOBN8R4yfI',
					size : 7430785494597966788,
					thumbs : array(
						$client->photoSizeEmpty(...),
						$client->photoSize(...),
						$client->photoCachedSize(...),
						$client->photoStrippedSize(...),
						$client->photoSizeProgressive(...),
						$client->photoPathSize(...),
					),
					video_thumbs : array(
						$client->videoSize(...),
						$client->videoSizeEmojiMarkup(...),
						$client->videoSizeStickerMarkup(...),
					),
					dc_id : 63,
					attributes : array(
						$client->documentAttributeImageSize(...),
						$client->documentAttributeAnimated(...),
						$client->documentAttributeSticker(...),
						$client->documentAttributeVideo(...),
						$client->documentAttributeAudio(...),
						$client->documentAttributeFilename(...),
						$client->documentAttributeHasStickers(...),
						$client->documentAttributeCustomEmoji(...),
					),
				),
			),
			settings : $client->themeSettings(
				message_colors_animated : true,
				base_theme : $client->baseThemeClassic(...),
				accent_color : 40,
				outbox_accent_color : 72,
				message_colors : array(96),
				wallpaper : $client->wallPaper(...),
			),
		),
		$client->webPageAttributeStory(
			peer : $client->peerUser(
				user_id : -5096776544512325759,
			),
			id : 9,
			story : $client->storyItemDeleted(
				id : 93,
			),
		),
		$client->webPageAttributeStickerSet(
			emojis : true,
			text_color : true,
			stickers : array(
				$client->documentEmpty(
					id : -185566655625017646,
				),
				$client->document(
					id : 571344431132751022,
					access_hash : -631920830705480878,
					file_reference : '??GLiveProto[X
?',
					date : 58,
					mime_type : 'QN78FKLUJ5EfmTv3',
					size : 7504493206715261312,
					thumbs : array(
						$client->photoSizeEmpty(...),
						$client->photoSize(...),
						$client->photoCachedSize(...),
						$client->photoStrippedSize(...),
						$client->photoSizeProgressive(...),
						$client->photoPathSize(...),
					),
					video_thumbs : array(
						$client->videoSize(...),
						$client->videoSizeEmojiMarkup(...),
						$client->videoSizeStickerMarkup(...),
					),
					dc_id : 13,
					attributes : array(
						$client->documentAttributeImageSize(...),
						$client->documentAttributeAnimated(...),
						$client->documentAttributeSticker(...),
						$client->documentAttributeVideo(...),
						$client->documentAttributeAudio(...),
						$client->documentAttributeFilename(...),
						$client->documentAttributeHasStickers(...),
						$client->documentAttributeCustomEmoji(...),
					),
				),
			),
		),
		$client->webPageAttributeUniqueStarGift(
			gift : $client->starGift(
				limited : true,
				sold_out : true,
				birthday : true,
				require_premium : true,
				limited_per_user : true,
				id : 5454585830826480534,
				sticker : $client->documentEmpty(...),
				stars : -2296347827844872934,
				availability_remains : 54,
				availability_total : 56,
				availability_resale : -6830292107100459843,
				convert_stars : 7719650389515015374,
				first_sale_date : 97,
				last_sale_date : 37,
				upgrade_stars : -4922954358599104432,
				resell_min_stars : 2087063422524442594,
				title : 'Q4cz2ux7CMISOhiw',
				released_by : $client->peerUser(...),
				per_user_total : 66,
				per_user_remains : 52,
			),
		),
		$client->webPageAttributeStarGiftCollection(
			icons : array(
				$client->documentEmpty(
					id : 22752053736412346,
				),
				$client->document(
					id : -6450867609127517917,
					access_hash : -4712645298637695158,
					file_reference : '??!??LiveProto??k[',
					date : 12,
					mime_type : 'mKiFA8jCoDkR4EOB',
					size : -5483449397287603451,
					thumbs : array(
						$client->photoSizeEmpty(...),
						$client->photoSize(...),
						$client->photoCachedSize(...),
						$client->photoStrippedSize(...),
						$client->photoSizeProgressive(...),
						$client->photoPathSize(...),
					),
					video_thumbs : array(
						$client->videoSize(...),
						$client->videoSizeEmojiMarkup(...),
						$client->videoSizeStickerMarkup(...),
					),
					dc_id : 99,
					attributes : array(
						$client->documentAttributeImageSize(...),
						$client->documentAttributeAnimated(...),
						$client->documentAttributeSticker(...),
						$client->documentAttributeVideo(...),
						$client->documentAttributeAudio(...),
						$client->documentAttributeFilename(...),
						$client->documentAttributeHasStickers(...),
						$client->documentAttributeCustomEmoji(...),
					),
				),
			),
		),
	),
);
```