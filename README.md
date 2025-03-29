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

> [!Tip]
> 不要相信任何的咸鱼卖CMS，或者部署CMS的，本程序没有授权给任何人销售。
 
> CMS 唯一TG的群 [**TG反馈群⁠**](https://t.me/+v08KwCO7jH0xNjZl)

## CMS-0.3.5.7 更新日志
1. 增加115、阿里云盘的文件夹、回收站定时清理；启用代表启动定时任务
2. alist同步支持定时任务
3. 修复Emby搜索有时会搜到演员的问题

## CMS-0.3.5.5-0.3.5.6 更新日志
1. 优化emby里手动删除时同步删除云盘文件（需要神医助手先把通知系统增强打开，再在通知里勾上媒体深度删除）
2. 修复文件夹重命名同步
3. 优化自动整理

注：慎用，不保证不会误删

## CMS-0.3.5.4 更新日志
1. 增加115分享同步（生成基于分享的strm）
2. 302日志增加文件名
3. 修复alist同步不通知emby刷新

注意：使用115分享直连播放时会自动保存一份到我的接收，所以请确保待整理文件夹不是我的接收

## CMS-0.3.5.3 更新日志
1. 增加alist同步通知、刷新入库
2. bot增加alist同步菜单（会同步所有路径）
3. 优化代码，增加稳定性

## CMS-0.3.5.2 更新日志
1. 修复alist同步视频大小过滤会过滤非视频
2. alist同步增加请求间隔
3. 修复115图片同步有时会同步失败的问题
4. 同步记录支持名称、时间排序

## CMS-0.3.5.1 更新日志
1. 增加alist同步
2. 全量同步增加最小视频过滤
3. 一些优化

## CMS-0.3.4.13 更新日志
1. 一些优化 应该是0.3.4最后一个版本了

## CMS-0.3.4.12 更新日志
1. 自动整理支持整理字幕（原字幕名必须为标准命名）
2. 修复部分情况下episode_name不可用的问题
3. 优化了中文标题的获取
4. 优化了阿里秒传的逻辑
5. 记的备份下cms-online.db文件，回退版本时会用到

## CMS-0.3.4.11 更新日志
1. 修正3410的BUG

## CMS-0.3.4.10 更新日志
1. 增强识别，修复GPT辅助识别的BUG
2. 命名规则支持 season_name、season_year、episode_name
3. 二级分类策略支持文件后缀匹配 ext

## CMS-0.3.4.9 更新日志
1. 增强识别
2. 支持黑名单和大小过滤
3. 电影名称为英文时，尝试获取中文名
4. 增加openai辅助识别
   
## CMS--0.3.4.5 → 0.3.4.8 更新日志
1. 自动整理增强识别

##CMS-0.3.4.4 更新日志
1. 增强识别
2. 修复剧集有时无法重命名

## CMS-0.3.4.3 更新日志
1. 自动整理去除MP依赖、更改了部分变量、注意先看下变量说明
2. 修复入库刷新有时会匹配不到数据库的问题
3. 升级前备份下cms-online.db文件，便于恢复
   
## CMS-0.3.3.13 更新日志
1. 修复快速模式图片、元数据不下载的问题
2. 升级P115，优化代码，增加稳定性
   
## CMS-0.3.3.12 更新日志
1. 分享链接兼容 115cdn.com
2. 升级P115，优化代码，增加稳定性

## CMS-0.3.3.11 更新日志
1. 剧集通知增加集数信息（需要在神医助手里打开）

## CMS-0.3.3.10 更新日志
1. 增加 IS_HK_VPS 环境变量，用于指定是否为香港VPS, IS_HK_VPS=1 为香港VPS（不是不需要加）
2. 优化代码，增加稳定性
   
## CMS-0.3.3.9 更新日志
1. 修改了获取待整理视频逻辑，请将待整理文件夹文件数限制为10000以内（待整理的文件或所在文件夹必须含有电影名称）
2. 优化代码，增加稳定性
   
## CMS-0.3.3.8 更新日志
1. 增加阿里秒传115文件夹cid配置
2. 优化代码，增加稳定性

## CMS-0.3.3.7 更新日志
1. 手动转存不再判断链接是否存在
2. 优化阿里订阅，不会再重复发送分享已取消
3. 升级p115，快速同步使用星标，实测20T的库，10000视频没风控（勇者可以试下，可以先备份cms-online.db，以便恢复）
4. 转存下载兼容32位磁力
5. 优化代码，增加稳定性

## CMS-0.3.3.5 更新日志
1. 升级p115，更换了一些接口，希望风控好些
   
## CMS-0.3.3.4 【此版本启动需要PRO】更新日志
1. 增加快速同步模式，10000个STRM只需要10秒（别用这个模式，风控太强现在）
2. 增加自定义图片下载线程
3. 增加自动刷新CK开关
4. 支持文件夹上传事件同步
5. 更换刷新媒体库方式，似乎更快了
6. 优化代码，增加稳定性
7. 暂时关闭免费版本

## CMS-0.3.2 更新日志
1. 增加同步记录管理
2. 优化emby入库通知，支持播放、暂停类通知
3. 修复部分剧集单集入库通知失败的问题
4. 修复自动整理文件夹存在时，创建失败的问题
5. 兼容没有昵称的阿里云盘账号登录

## CMS-0.3.1.2 更新日志
1. strm生成时自动通知emby进行扫库，支持高级配置
2. 增加cms同步结果通知
3. 修复剧集1-10集存在时，重复入库的问题
4. 修复热门推荐剧集搜索年份不生效的问题
5. EMBY_HOST_PORT、EMBY_API_KEY改为必填

## CMS-0.3.1 更新日志
1. 增加emby入库通知（PRO），emby通知设为 http://172.17.0.1:9527/api/emby/webhook?token=cloud_media_sync
2. strm生成时自动通知emby进行扫库
3. 消息通知增加TG机器人（PRO），调整了企业微信的配置页面，需要重新配置，请重新保存下核心配置（很重要）
4. 增加CMS_API_TOKEN变量，用于指定cms的api token，默认为cloud_media_sync
5. 修复文件名过长，导致整个任务直接结束的问题
6. 修复视频文件移动失败的问题
7. 如果页面上看不到更新，就强刷下页面，清下缓存

## CMS-0.3.0.7 更新日志
1. 重新打包授权，必须更新

## CMS-0.3.0.6 更新日志
1. 修复日志文件过大的问题，请先删除cms.log这个日志文件，再更新
2. 内存占用过大的问题没找到原因，请有这个问题的朋友私聊我

## CMS-0.3.0.5 更新日志
1. 修复生活事件同步有时会缺失的问题
2. 修复阿里云盘分享没有文件夹会失败的问题
3. 修改代理地址的变量名，请在核心配置里重新配置

## CMS-0.3.0.3 更新日志
1. 修复阿里云盘不可用（请重新扫码登录，重新在资源库创建文件夹（如果获取路径失败就在备份盘创建文件夹，原因看图），并填写新的文件夹id）
2. 修复重复订阅
   
## CMS-0.3.0.2 更新日志
1. 修复元数据下载失败
2. 修复时间显示不正常（只对新数据有效）
3. 尝试支持ipv6
4. 尝试修复阿里云盘不可用

## CMS-0.3.0 更新日志
1. 页面增加实时日志显示
2. 增加转存下载，支持115分享、磁力、ed2k、阿里云盘分享（会自动秒传到115），配合自动整理效果更佳
3. 增加订阅功能，支持订阅tg的115或阿里云资源频道
4. 企业微信支持接收转存下载格式的消息
注：2、3、4为PRO版功能，免费版不支持
