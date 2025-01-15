# Cloud Media Sync
<div align="center">
   
![](https://github.com/user-attachments/assets/e137ba0b-43b4-477b-bae8-27b7cbf91cff)

## [English][[中文]](README.md)

</div>
  
## Cloud Media Sync Update Notes
> [!IMPORTANT]  
> Docker Image: [`cloud-media-sync`](https://hub.docker.com/r/imaliang/cloud-media-sync)  
> Help and Documentation: [`Wiki`](https://github.com/guyue2005/CMSHelp/wiki)

## Introduction
**cloud-media-sync (CMS)** — Cloud media library synchronization tool

> Monitors the `115` folder and generates `strm` files recognized by `emby`, supporting incremental updates and `emby302`.

> This project is based on [`python-115`](https://github.com/ChenyangGao/web-mount-packs), which is very powerful for those who understand the code.

> Thanks to: `尽贫·禁评` `DDSRem`

> Thanks to: `Black_Plum` `HuLuXi` for providing container installation tutorials.

> [**TG Feedback Group**](https://t.me/+v08KwCO7jH0xNjZl)


## cloud-media-sync-0.3.3.1 【PRO required to start this version】 Update Log
1. Added fast sync mode, syncing 10,000 STRM files in just 10 seconds.
2. Added custom image download threads.
3. Added automatic CK refresh toggle.
4. Supports folder upload event synchronization.
5. Changed media library refresh method, seems faster now.
6. Optimized code to improve stability.
7. Temporarily disabled the free version.

## cloud-media-sync-0.3.2 Update Log
1. Added synchronization record management
2. Optimized Emby library notification, supporting play and pause notifications
3. Fixed issue where single episode library notifications failed for some series
4. Fixed issue where folder creation failed when automatic folder organization was enabled
5. Made compatible with Aliyun Pan accounts without a nickname for login


## cloud-media-sync-0.3.1.2 Update Log
1. Automatically notify Emby to scan the library when generating strm files, supporting advanced configuration.
2. Added CMS synchronization result notifications.
3. Fixed the issue of duplicate entries when episodes 1-10 already exist.
4. Fixed the issue of the year filter not working for popular recommended series.
5. EMBY_HOST_PORT and EMBY_API_KEY are now required fields.

## cloud-media-sync-0.3.1 Update Log
1. Added Emby library import notifications (PRO), set the Emby webhook to `http://172.17.0.1:9527/api/emby/webhook?token=cloud_media_sync`.
2. Automatically notify Emby to scan the library when generating strm files.
3. Added Telegram Bot notifications (PRO), adjusted the corporate WeChat configuration page. Please reconfigure and save the core settings (very important).
4. Added CMS_API_TOKEN variable to specify the CMS API token (default is `cloud_media_sync`).
5. Fixed the issue where tasks would terminate if the file name is too long.
6. Fixed the issue of video file move failures.
7. If updates are not visible on the page, please force refresh the page and clear the cache.

## cloud-media-sync-0.3.0.7 Update Log
1. Repackaged authorization, update is required.

## cloud-media-sync-0.3.0.6 Update Log
1. Fixed the issue of oversized log files. Please delete the `cms.log` file before updating.
2. The issue of excessive memory usage is still under investigation. If you are experiencing this issue, please contact me privately.

## cloud-media-sync-0.3.0.5 Update Log
1. Fixed the issue where life events synchronization would sometimes fail.
2. Fixed the issue where sharing Aliyun Drive would fail without a folder.
3. Changed the variable name for the proxy address. Please reconfigure it in the core settings.

## cloud-media-sync-0.3.0.3 Update Log
1. Fixed the issue where Aliyun Drive was unavailable (please rescan login, create a folder in the resource library again (if path fetching fails, create the folder in the backup disk as per the diagram), and input the new folder ID).
2. Fixed the issue of duplicate subscriptions.

## cloud-media-sync-0.3.0.2 Update Log
1. Fixed the issue of metadata download failure.
2. Fixed abnormal time display (only applies to new data).
3. Attempted to support IPv6.
4. Attempted to fix Aliyun Drive unavailability.

## cloud-media-sync-0.3.0 Update Log
1. Added real-time log display to the page.
2. Added download transfer feature, supporting 115 share, magnet links, ed2k, and Aliyun Drive sharing (automatically seeding to 115). Best used with automatic sorting.
3. Added subscription feature, supporting subscribing to 115 or Aliyun cloud resource channels on TG.
4. Corporate WeChat now supports receiving transfer/download message formats.

**Note:** Features 2, 3, and 4 are only available in the PRO version. Free version does not support these.
