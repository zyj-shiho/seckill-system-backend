# 🛒 电商秒杀系统后端

基于 Spring Boot 3 + Redis + RabbitMQ 的高并发秒杀系统，用于学习分布式架构、性能优化、高可用设计。

## 🚀 技术栈

| 技术 | 用途 |
|------|------|
| Java 21 | 主语言（LTS 长期支持） |
| Spring Boot 3.5.5 | 快速开发框架 |
| MyBatis | 数据库 ORM |
| MySQL | 商品、订单、用户数据 |
| Redis | 缓存热点商品、库存、分布式锁 |
| RabbitMQ | 异步下单、解耦、削峰 |
| Lombok | 简化实体类代码 |
| Maven | 项目构建 |
| Spring Cache | 缓存注解 |
| Validation | 参数校验 |

## 📦 本地启动

### 1. 启动依赖服务（Docker 推荐）

```bash
# 启动 MySQL
docker run -d --name mysql-seckill -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 mysql:8.0

# 启动 Redis
docker run -d --name redis-seckill -p 6379:6379 redis:7

# 启动 RabbitMQ（带管理界面）
docker run -d --name rabbitmq-seckill -p 5672:5672 -p 15672:15672 rabbitmq:3-management