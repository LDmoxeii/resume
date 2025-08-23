# Java后端开发实习

> <span class="icon">&#xe60f;</span> `(86)159-7678-1430` <span>&emsp;</span> <span class="icon">&#xe7ca;</span> `15976781430@163.com` <span>&emsp;</span> <span class="icon">&#xe600;</span> [LDmoxeii](https://github.com/LDmoxeii)

<img class="avatar" src="avatar.jpg">

## <span>&#xe80c;</span> 教育经历

<div class="entry-title">
    <h3>广州软件学院 - 本科 - 软件工程专业</h3> 
    <p>2022.09 - 2026.07</p>
</div>

**英语水平：** CET-4

**竞赛获奖：**
- 2024年美国大学生数学建模比赛国家级二等奖
- 第十五届蓝桥杯全国软件和信息技术专业人才大赛广东赛区程序设计大学B组三等奖

## <span>&#xe618;</span> 工作经验

<div alt="entry-title">
    <h3>Java后端开发实习 - 元盟科技有限公司</h3> 
    <p>2025.03 - 至今</p>
</div>

**主要参与项目:** BOSS(业务运营支撑系统)  
**负责模块:** BASIC(基础通用数据)、CRM(客户关系管理)、PCS(权限控制服务)、UAA(统一账号与认证体系) 服务。

**核心贡献：**
- **权限资源跨环境同步**
  - 设计 **可排序多叉树** 数据结构，实现 **数据库扁平结构到内存树形结构** 的转换
  - 支持任意位置资源插入、删除、更新、移动，保持操作独立性和健壮性
  - 通过 **RPC(远程服务调用)** 配合 **非对称加密**，确保跨环境同步安全性
  - 使用 **gzip** 优化同步信息传输，提高 **15%** IO效率
  - 使用 **CompletableFuture** 并发获取不同环境资源，提高 **40%** 执行效率
  - 显著提升 **80%** 下游开发人员资源维护效率，稳定运行4个月
  - 工具类引用数 **99+**，获得开发团队好评

## <span>&#xe635;</span> 项目经历

<div class="entry-title">
    <h3>only4-KSP-cap4j（知享汇）</h3>
    <a href="https://github.com/LDmoxeii/only4-KSP-cap4j">github.com/LDmoxeii/only4-KSP-cap4j</a>
</div>

基于cap4j框架和DDD设计思想实现的知识分享社交平台，提供用户加入兴趣群组、获取特定领域知识和交流机会的完整业务流程。
- **技术栈：** SpringBoot、MySQL、Mybatis-Plus、Redis、Redisson
- **多级缓存架构：** 使用策略模式扩展多种登录方式，**Redis** + **Caffeine** 实现用户信息多级缓存
- **防重系统：** 参考美团GTIS系统，通过 **AOP** + **Redis** 缓存验证防止重复请求
- **缓存一致性：** 采用 **Cache Aside** 模式并通过Spring Cache注解解决数据库与缓存一致性问题
- **秒杀系统：** 利用 **Redis** + **Lua** 脚本预检用户资格，结合乐观锁防止优惠券超卖
- **分布式锁：** 基于 **Redis** 分布式锁确保集群环境下一人一单的线程安全
- **延迟队列：** 使用 **RabbitMQ** 延迟队列实现超时支付自动关单

<div class="entry-title">
    <h3>Cap4k</h3>
    <a href="https://github.com/LDmoxeii/cap4k">github.com/LDmoxeii/cap4k</a>
</div>

基于 **整洁架构**、**中介者模式**、**发件箱模式**、**CQS命令查询分离** 等设计理念的企业级开发框架。
- **技术栈：** SpringBoot、Mybatis-Plus、Redisson、Spring-Data-JPA
- **架构设计：** 使用 **端口适配器模式** 实现整洁架构中 **定义与实现** 的分离
- **数据处理：** **工作单元模式** 实现数据持久化批次处理，支持DDD核心概念的 **整存**
- **中介器模式：** 简化 **IoC** 依赖注入，加快开发流程
- **事件一致性：** **发件箱模式** 保证DDD设计中 **领域事件** 的 **最终一致性**
- **认证系统：** **策略模式** 实现灵活扩展的登录流程（账号密码、邮箱、手机验证码）
- **安全防护：** **Redis** 缓存防登录攻击、AOP+Redis **防重幂等**、Redisson **限流**
- **权限管理：** **RBAC模型** 支持细粒度权限管理和数据权限控制

## <span>&#xe635;</span> 开源贡献

<div class="entry-title">
    <h3>cap4j - Java企业级DDD领域驱动设计战术框架</h3> 
    <a href="https://github.com/netcorepal/cap4j">github.com/netcorepal/cap4j</a>
</div>

- 参与框架核心功能的设计与实现
- 提供代码优化建议和性能改进方案
- 为开源社区贡献高质量代码

## <span>&#xecfa;</span> 专业技能

### 编程基础
- **Java核心：** 集合框架、Stream流、反射机制、多线程编程、SPI机制
- **并发编程：** CAS、AQS、并发集合、阻塞队列等工具及其实现原理
- **JVM：** 内存模型、类加载机制、垃圾回收机制、运行时数据区
- **数据结构：** 栈、队列、链表、二叉树等常用数据结构

### 数据库
- **MySQL：** 索引优化、事务机制、MVCC、锁机制，具备慢SQL优化经验
- **Redis：** 数据结构、持久化、高可用机制、缓存雪崩/穿透/击穿解决方案、分布式锁

### 系统设计
- **设计模式：** 策略模式、工厂模式、模板模式、责任链模式、代理模式等
- **架构思想：** DDD领域驱动设计、TDD测试驱动设计、整洁架构
- **分布式：** 分布式锁、分布式事务、服务注册发现、负载均衡

### 框架技术
- **Spring生态：** SpringBoot、MyBatis、Spring AOP、IoC、自动装配机制
- **微服务：** SpringCloud、SpringCloudAlibaba
- **持久层：** MyBatis、Spring-Data-JPA，熟悉ORM映射
- **源码阅读：** 阅读过mini-spring源码，理解框架设计思想

### 中间件与工具
- **消息队列：** RabbitMQ（消息可靠性、重复消费、死信队列等）
- **开发工具：** Git版本控制、IDEA、Maven构建工具
- **运维：** Linux常用命令、Docker基本操作