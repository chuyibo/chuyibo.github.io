---
layout: post
category: Java
title: SpringBoot 总结
tags: Android
keywords: Android
excerpt: 简介摘要
redirect_from:
  - /2020/26/about/
---

### 工程创建

<hr/>

- 添加 Maven 依赖

```
<parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>2.1.5.RELEASE</version>
</parent>

// 未指定版本号，在父工程中已经对版本进行了管理
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
</dependencies>
```

- 创建启动类

```
@org.springframework.boot.autoconfigure.SpringBootApplication
public class SpringBootApplication {

    public static void main(String[] args) {
        SpringApplication.run(SpringBootApplication.class, args);
    }
}
```

- 创建 Controller

```
@RestController
public class TestController {

    @GetMapping("test")
    public String test() {
        return "Hello World!";
    }
}
```

