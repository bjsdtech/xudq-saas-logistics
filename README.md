## 数动物流货运服务介绍

`xudq-saas-logistics`是一套基于微服务技术架构的物流货运系统，前端后端分离部署，采用了 Vue、Spring Boot、MyBatis、Docker、Elasticsearch等核心技术快速搭建系统。

## 业务功能
``` lua
业务体系支持：
物流货运服务模块
1、业务中心
   ├── 后台管理：用户管理、角色管理、权限管理、日志管理...
   ├── 客户管理：个人客户、企业客户...
   ├── 仓储管理：仓库管理、区域管理、进出管理、消费管理、环境管理...
   ├── 运输管理：车队管理、车辆管理、司机管理、导航管理、线路管理、节点管理...
   ├── 包装管理：包装类型、包装详情...
   ├── 装卸搬运管理：
   ├── 配送管理：运单管理、提货管理、车辆配载、送货管理、签收管理、在途监控...
2.财会中心（支持对接xudq-saas-accounting SaaS服务 [https://github.com/bjsdtech/xudq-saas-accounting.git]）。
   ├── 财务管理：对账调账、资金流水、账务锁账、财务审批...
   ├── 会计管理：账套管理、期间管理、科目管理、凭证管理...
   ├── 报表管理：财务报表、会计报表、账务报表、时效报表...

```

## 系统模块结构
``` lua
logistics -- 父项目
├── logistics-common -- 通用代码模
├── logistics-utils -- 工具类模块
├── logistics-api -- 公共接口模块
├── logistics-admin -- 管理后台
├── logistics-customer -- 客户模块
├── logistics-storage -- 仓储模块
├── logistics-transport -- 运输模块
├── logistics-carry -- 搬运模块
├── logistics-pack -- 包装模块
├── logistics-delivery -- 交付模块
├── logistics-finance -- 财务模块
├── logistics-accounting -- 会计模块
├── logistics-statements -- 报表模块
├── logistics-security -- 封装SpringSecurity+JWT的安全认证的模块
├── logistics-search -- 基于Elasticsearch的商品搜索系统服务模块
├── logistics-cache -- 基于 Redis 分布式缓存服务模块
├── logistics-mq --  基于RocketMQ的消息队列服务模块
```



## 技术选型


### 前端技术

| 技术       | 说明                  | 官网                                                         |
| ---------- | --------------------- | ------------------------------------------------------------ |
| Vue        | 前端框架              | [https://vuejs.org/](https://vuejs.org/)                     |
| Vue-router | 路由框架              | [https://router.vuejs.org/](https://router.vuejs.org/)       |
| Vuex       | 全局状态管理框架      | [https://vuex.vuejs.org/](https://vuex.vuejs.org/)           |
| Element    | 前端UI框架            | [https://element.eleme.io/](https://element.eleme.io/)       |
| Axios      | 前端HTTP框架          | [https://github.com/axios/axios](https://github.com/axios/axios) |
| v-charts   | 基于Echarts的图表框架 | [https://v-charts.js.org/](https://v-charts.js.org/)         |

### 后端技术

| 技术                 | 说明                | 官网                                                         |
| -------------------- | ------------------- | ------------------------------------------------------------ |
| Spring Boot          | 容器+MVC框架        | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot) |
| Spring Security      | 认证和授权框架      | [https://spring.io/projects/spring-security](https://spring.io/projects/spring-security) |
| MyBatis              | ORM框架             | [http://www.mybatis.org/mybatis-3/zh/index.html](http://www.mybatis.org/mybatis-3/zh/index.html) |
| MyBatisGenerator     | 数据层代码生成      | [http://www.mybatis.org/generator/index.html](http://www.mybatis.org/generator/index.html) |
| PageHelper           | MyBatis物理分页插件 | [http://git.oschina.net/free/Mybatis_PageHelper](http://git.oschina.net/free/Mybatis_PageHelper) |
| Swagger-UI           | 文档生产工具        | [https://github.com/swagger-api/swagger-ui](https://github.com/swagger-api/swagger-ui) |
| Elasticsearch        | 搜索引擎            | [https://github.com/elastic/elasticsearch](https://github.com/elastic/elasticsearch) |
| RocketMQ             | 消息队列            | [https://rocketmq.apache.org](https://github.com/apache/rocketmq)         |
| Redis                | 分布式缓存          | [https://redis.io/](https://redis.io/)                       |
| MongoDb              | NoSql数据库         | [https://www.mongodb.com/](https://www.mongodb.com/)         |
| Docker               | 应用容器引擎        | [https://www.docker.com/](https://www.docker.com/)           |
| Druid                | 数据库连接池        | [https://github.com/alibaba/druid](https://github.com/alibaba/druid) |
| OSS                  | 对象存储            | [https://github.com/aliyun/aliyun-oss-java-sdk](https://github.com/aliyun/aliyun-oss-java-sdk) |
| JWT                  | JWT登录支持         | [https://github.com/jwtk/jjwt](https://github.com/jwtk/jjwt) |
| LogStash             | 日志收集            | [https://github.com/logstash/logstash-logback-encoder](https://github.com/logstash/logstash-logback-encoder) |
| Lombok               | 简化对象封装工具    | [https://github.com/rzwitserloot/lombok](https://github.com/rzwitserloot/lombok) |
| Seata                | 全局事务管理框架    | [https://github.com/seata/seata](https://github.com/seata/seata) |
| Portainer            | 可视化Docker容器管理| [https://github.com/portainer/portainer](https://github.com/portainer/portainer) |


## 环境搭建

### 开发环境

工具 | 版本号 | 下载
----|----|----
JDK | 1.8 | https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
Mysql | 5.8 | https://www.mysql.com/
Redis | 3.2 | https://redis.io/download
Elasticsearch | 6.2.2 | https://www.elastic.co/downloads
MongoDb | 3.2 | https://www.mongodb.com/download-center
RocketMQ | 3.9.1 | https://rocketmq.apache.org/download/
nginx | 1.10 | http://nginx.org/en/download.html

## 联系方式
Email：2558404588@qq.com

