# Cloud Media Sync
<div align="center">
   
![](https://github.com/user-attachments/assets/e137ba0b-43b4-477b-bae8-27b7cbf91cff)


## [中文][[English]](README.en.md)

</div>

## Cloud Media Sync 更新说明
> [!IMPORTANT]
> Docker 地址:[`cloud-media-sync`](https://hub.docker.com/r/imaliang/cloud-media-sync)  帮助 说明查看 [`Wiki`](https://github.com/guyue2005/CMSHelp/wiki)
## 简介
cloud-media-sync（CMS）--- 云端媒体库同步工具

> 监控`115`文件夹，生成`emby`可以识别的`strm`文件，支持增量，支持`emby302`。

> 本项目基于 [`python-115`](https://github.com/ChenyangGao/web-mount-packs)，懂代码的可以看看，非常强大。

> 致谢：`尽贫·禁评` `DDSRem`

> 致谢：`Black_Plum` `HuLuXi` 提供相关容器安装环境教程

> [**TG反馈群⁠**](https://t.me/+v08KwCO7jH0xNjZl)

## cloud-media-sync-0.3.2 更新日志
1. 增加同步记录管理
2. 优化emby入库通知，支持播放、暂停类通知
3. 修复部分剧集单集入库通知失败的问题
4. 修复自动整理文件夹存在时，创建失败的问题
5. 兼容没有昵称的阿里云盘账号登录

## cloud-media-sync-0.3.1.2 更新日志
1. strm生成时自动通知emby进行扫库，支持高级配置
2. 增加cms同步结果通知
3. 修复剧集1-10集存在时，重复入库的问题
4. 修复热门推荐剧集搜索年份不生效的问题
5. EMBY_HOST_PORT、EMBY_API_KEY改为必填

## cloud-media-sync-0.3.1 更新日志
1. 增加emby入库通知（PRO），emby通知设为 http://172.17.0.1:9527/api/emby/webhook?token=cloud_media_sync
2. strm生成时自动通知emby进行扫库
3. 消息通知增加TG机器人（PRO），调整了企业微信的配置页面，需要重新配置，请重新保存下核心配置（很重要）
4. 增加CMS_API_TOKEN变量，用于指定cms的api token，默认为cloud_media_sync
5. 修复文件名过长，导致整个任务直接结束的问题
6. 修复视频文件移动失败的问题
7. 如果页面上看不到更新，就强刷下页面，清下缓存

## cloud-media-sync-0.3.0.7 更新日志
1. 重新打包授权，必须更新

## cloud-media-sync-0.3.0.6 更新日志
1. 修复日志文件过大的问题，请先删除cms.log这个日志文件，再更新
2. 内存占用过大的问题没找到原因，请有这个问题的朋友私聊我

## cloud-media-sync-0.3.0.5 更新日志
1. 修复生活事件同步有时会缺失的问题
2. 修复阿里云盘分享没有文件夹会失败的问题
3. 修改代理地址的变量名，请在核心配置里重新配置

## cloud-media-sync-0.3.0.3 更新日志
1. 修复阿里云盘不可用（请重新扫码登录，重新在资源库创建文件夹（如果获取路径失败就在备份盘创建文件夹，原因看图），并填写新的文件夹id）
2. 修复重复订阅
   
## cloud-media-sync-0.3.0.2 更新日志
1. 修复元数据下载失败
2. 修复时间显示不正常（只对新数据有效）
3. 尝试支持ipv6
4. 尝试修复阿里云盘不可用

## cloud-media-sync-0.3.0 更新日志
1. 页面增加实时日志显示
2. 增加转存下载，支持115分享、磁力、ed2k、阿里云盘分享（会自动秒传到115），配合自动整理效果更佳
3. 增加订阅功能，支持订阅tg的115或阿里云资源频道
4. 企业微信支持接收转存下载格式的消息
注：2、3、4为PRO版功能，免费版不支持
