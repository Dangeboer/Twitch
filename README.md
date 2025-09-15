# 🎮 智能游戏直播推荐平台

一个基于 **Spring Boot** 构建的全栈游戏直播与视频平台，支持用户注册、关键词搜索、浏览与收藏，并基于收藏记录实时推荐个性化视频。项目通过缓存、推荐算法与云部署优化，提供高效、稳定的游戏直播与视频观看体验。

## ✨ 功能特性

- **用户管理**：支持注册、登录与会话管理  
- **安全认证**：基于 Spring Security 的认证与授权，限制部分 API 的访问权限  
- **内容搜索**：支持关键词搜索 Twitch 平台的直播与视频资源  
- **个性化推荐**：基于用户收藏记录，智能推荐相关直播与视频  
- **收藏功能**：用户可收藏喜欢的内容，形成个性化推荐依据  
- **缓存优化**：对热门游戏、搜索结果与收藏记录进行缓存，加速响应  
- **容器化与部署**：Docker 模拟 MySQL 数据库环境，服务部署至 AWS  

## 🛠 技术栈

- **后端框架**：Spring Boot, Spring Security, Spring Cloud OpenFeign  
- **数据库**：MySQL (Docker 环境)  
- **缓存**：Caffeine Cache  
- **第三方服务**：Twitch API  
- **容器化与部署**：Docker, AWS  

## 📐 系统架构

```mermaid
graph TD
    User[用户] -->|HTTP| Backend[Spring Boot Service]
    Backend -->|认证/授权| Security[Spring Security]
    Backend -->|Feign| TwitchAPI[(Twitch API)]
    Backend -->|缓存| Caffeine[(Caffeine Cache)]
    Backend -->|存储| MySQL[(MySQL - Docker)]
    Backend -->|部署| AWS[(AWS Cloud)]
