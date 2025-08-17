# account.autoDownloadSettings

**Description** : *Media autodownload settings*

**Layer** : 211

```tl
account.autoDownloadSettings#63cacf26 low:AutoDownloadSettings medium:AutoDownloadSettings high:AutoDownloadSettings = account.AutoDownloadSettings;
```

---

## Parameters

| Name | Type | Description |
| :---: | :---: | :--- |
| <mark>low</mark> | [`AutoDownloadSettings`](type/AutoDownloadSettings) | Low data usage preset |
| <mark>medium</mark> | [`AutoDownloadSettings`](type/AutoDownloadSettings) | Medium data usage preset |
| <mark>high</mark> | [`AutoDownloadSettings`](type/AutoDownloadSettings) | High data usage preset |

---

## Type

[account.AutoDownloadSettings](type/account.AutoDownloadSettings)

---

## Example

```php
$accountAutoDownloadSettings = $client->account->autoDownloadSettings(
	low : $client->autoDownloadSettings(
		disabled : true,
		video_preload_large : true,
		audio_preload_next : true,
		phonecalls_less_data : true,
		stories_preload : true,
		photo_size_max : 28,
		video_size_max : -8182431891471397057,
		file_size_max : 3235858436368394535,
		video_upload_maxbitrate : 85,
		small_queue_active_operations_max : 2,
		large_queue_active_operations_max : 28,
	),
	medium : $client->autoDownloadSettings(
		disabled : true,
		video_preload_large : true,
		audio_preload_next : true,
		phonecalls_less_data : true,
		stories_preload : true,
		photo_size_max : 61,
		video_size_max : -5593275028793430366,
		file_size_max : -562609154075612981,
		video_upload_maxbitrate : 81,
		small_queue_active_operations_max : 1,
		large_queue_active_operations_max : 63,
	),
	high : $client->autoDownloadSettings(
		disabled : true,
		video_preload_large : true,
		audio_preload_next : true,
		phonecalls_less_data : true,
		stories_preload : true,
		photo_size_max : 87,
		video_size_max : -5995574652839122951,
		file_size_max : 1564845211275713994,
		video_upload_maxbitrate : 12,
		small_queue_active_operations_max : 97,
		large_queue_active_operations_max : 16,
	),
);
```