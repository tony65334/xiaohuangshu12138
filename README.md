# 小黄书（xiaohuangshu）

## 项目简介
小黄书是一个基于Go语言开发的现代化多媒体内容管理与分发平台，支持视频、图片、笔记的上传、转码、存储、评论、点赞、关注、推荐等全方位社交功能，适合搭建自有内容社区或短视频平台。
##
[加入 Telegram 群](https://t.me/xiaohuangshu10)

## 主要功能
<p>
  <img src="https://github.com/user-attachments/assets/e55e0f33-1647-4b21-acde-ca492a4bd17d" width="40%" />
  <img src="https://github.com/user-attachments/assets/c1d87368-8560-41c2-b5db-3df16aeb612d" width="40%" />
</p>
<p>
  <img src="https://github.com/user-attachments/assets/339e813f-5c31-40fc-b3ce-87b8106f3941" width="40%" />
  <img src="https://github.com/user-attachments/assets/f51fa5cc-e9ce-4810-91cb-ad2ccbf0c723" width="40%" />
</p>


### 用户系统
- 用户注册、登录与JWT鉴权
- 头像上传与管理（自动转码为WebP格式）
- 用户关注/取消关注功能
- 关注列表和粉丝列表查看
- 用户资料管理

### 内容管理
- **视频功能**：视频上传、转码（支持HLS、MP4等格式）、播放、管理
- **笔记功能**：图文笔记上传、多图片支持、标签管理
- **评论系统**：支持对视频、笔记的评论与回复
- **点赞系统**：支持对视频、笔记、评论的点赞/取消点赞
- **标签管理**：内容分类与标签系统
- **搜索功能**：全文搜索支持

### 智能推荐
- 集成Gorse推荐系统
- 个性化内容推荐
- 管理员推荐内容管理
- 推荐算法优化

### 系统功能
- WebSocket实时通信
- 任务队列处理（转码、消息推送、清理等）
- 转码队列状态监控
- 缓存管理与清理
- 限流、日志、安全等中间件支持
- MinIO对象存储集成
- 支持多环境配置（dev/prod）
- SQL注入防护

## 技术栈
- **语言**：Go 1.24+
- **Web框架**：Gin
- **ORM**：GORM（MySQL驱动）
- **任务队列**：Asynq（基于Redis）
- **对象存储**：MinIO
- **缓存与队列**：Redis
- **推荐系统**：Gorse
- **配置管理**：Viper
- **JWT认证**：golang-jwt/jwt/v5
- **WebSocket**：gorilla/websocket
- **依赖管理**：Go Modules

## 环境要求
- Go 1.24 及以上
- MySQL 5.7+/8.0+（用于存储用户、视频、评论等数据）
- Redis 6.0+（用于缓存和任务队列）
- MinIO（或兼容S3的对象存储）
- Gorse推荐系统（可选）
- ffmpeg（用于视频转码，需本地安装并配置环境变量）

## 配置说明
所有配置项均可在 `configs/app.yaml` 文件中调整，包括：

### 基础配置
- 服务端口、环境模式、JWT密钥、令牌有效期
- 存储路径、上传大小限制、临时目录
- 限流参数

### 数据库配置
- Redis连接信息（缓存和任务队列）
- MySQL连接信息（主数据库）
- MinIO对象存储配置

### 业务配置
- 视频转码参数（输出格式、分片时长、编码器等）
- Gorse推荐系统配置
- 文件上传限制和路径配置

## 启动方式

### 1. 环境准备
```bash
# 安装依赖
go mod tidy

# 确保以下服务已启动：
# - MySQL数据库
# - Redis服务
# - MinIO对象存储
# - Gorse推荐系统（可选）
```

<a href="https://ccyy12.com/" target="_blank">策驰影院</a>
<a href="https://ccyy10.com/" target="_blank">策驰影院</a>
<a href="https://khsp.buzz/" target="_blank">快活视频</a>
<a href="https://xkyy11.com/" target="_blank">星空影院</a>
<a href="https://xkyy10.com/" target="_blank">星空影院</a>
