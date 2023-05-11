[中文](README.md) |
[ENGLISH](README_EN.md)

# 使用

1. 启动jaeger

```shell
$ docker run -d --name jaeger \
  -e COLLECTOR_ZIPKIN_HTTP_PORT=9411 \
  -p 5775:5775/udp \
  -p 6831:6831/udp \
  -p 6832:6832/udp \
  -p 5778:5778 \
  -p 16686:16686 \
  -p 14268:14268 \
  -p 9411:9411 \
  jaegertracing/all-in-one:1.6
```

2. 项目中引入相关依赖

```xml
<dependency>
    <groupId>io.github.linyimin0812</groupId>
    <artifactId>spring-bean-timeline</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
```

# 效果

点击http://127.0.0.1:16686 查看效果

![](./docs/spring-bean-timeline.jpg)

