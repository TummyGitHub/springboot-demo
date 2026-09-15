# com.tummy.springboot

基于 **Spring Boot 3** 的后端项目模板，用于快速搭建 Java 17 的 Web 服务，可作为后续业务项目的起手骨架。

## 技术栈

| 组件 | 版本 |
| --- | --- |
| JDK | 17 |
| Spring Boot | 3.0.6 |
| 构建工具 | Maven |
| Web 容器 | 内嵌 Tomcat（由 `spring-boot-starter-web` 提供） |

## 快速开始

```bash
# 开发模式启动，默认监听 http://localhost:8080
mvn spring-boot:run

# 打包为可执行 jar
mvn clean package
java -jar target/com_tummy_springboot-0.0.1-SNAPSHOT.jar

# 运行测试
mvn test
```

## 项目结构

```
.
├── pom.xml
└── src
    ├── main
    │   ├── java/com/tummy/springboot
    │   │   └── Application.java        # 启动类，@SpringBootApplication
    │   └── resources
    │       └── application.properties  # 应用配置
    └── test/java/com/tummy/springboot
        └── ApplicationTests.java       # 上下文加载测试
```

## 下一步

当前仅包含可运行的最小骨架，后续可在 `src/main/java/com/tummy/springboot` 下按 `controller` / `service` / `mapper` 分层扩展业务，并按需引入 `spring-boot-starter-data-jpa`、`mybatis-spring-boot-starter` 等依赖。
