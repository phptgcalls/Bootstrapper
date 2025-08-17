# bots.checkDownloadFileParams

**Description** : *Check if a mini app can request the download of a specific file: called when handling web_app_request_file_download events »*

**Layer** : 211

```tl
bots.checkDownloadFileParams#50077589 bot:InputUser file_name:string url:string = Bool;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>bot</mark> | [`InputUser`](type/InputUser) | The bot that owns the mini app that requested the download |
| <mark>file_name</mark> | [`string`](type/string) | The filename from the web_app_request_file_download event » |
| <mark>url</mark> | [`string`](type/string) | The url from the web_app_request_file_download event » |

---

## Result

[Bool](type/Bool)

---

## Possible Errors

| Type | Code | Description |
| :---: | :---: | :--- |
| **BOT_INVALID** | `400` | This is not a valid bot |

---

## Example

```php
$bool = $client->bots->checkDownloadFileParams(
	bot : $client->inputUserEmpty(),
	file_name : 'BX9ZnVHwi3G2Wcpo',
	url : 'https://docs.liveproto.dev',
);
```