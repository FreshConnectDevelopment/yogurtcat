# yogurtcat-server-system
yogurtcat-server-system项目是一个基于spring boot搭建的管理后台脚手架，目的是帮助开发人员聚焦业务开发快速完成业务交付。
## 特性列表
- 基于Flyway的数据库版本管理  
- 支持构建deb安装包 ，通过安装包部署服务器

## 功能列表
- 用户管理：提供用户的相关配置，新增用户后，默认密码为123456
- 角色管理：对权限与菜单进行分配，可根据部门设置角色的数据权限
- 菜单管理：已实现菜单动态路由，后端可配置化，支持多级菜单
- 操作日志：记录用户操作的日志
- 异常日志：记录异常日志，方便开发人员定位错误

### 配置文件（开发指导临时存放）
- spring启动配置文件  
spring启动配置文件提供了三种场景，具体说明如下
    - application-dev.yml  
    开发阶段数据库采用内存数据库H2的mysql模式，开发人员可以启动后就可以调试程序没有额外的数据库依赖
    - application-test.yml
    - application-prod.yml

## 十年期ssl证书生成
keytool -genkey -alias yogurtcat -keyalg RSA -validity 3650 -keystore yogurtcat.keystore
