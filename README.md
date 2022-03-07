# soapui

> soap 客户端

------


## 简介

因此构件的官方组织/作者已放弃维护，且在 maven 中央仓库无法下载原版，故有了此项目。

因没有源码（也无法编译），故是使用以下命令直接上传到 sonatype 的中央仓库：

```shell
mvn deploy:deploy-file \
 -DgroupId=com.exp-blog \
 -DartifactId=soapui \
 -Dversion=1.7.1 \
 -Dpackaging=jar \
 -Dfile=`pwd`/soapui-1.7.1.jar \
 -Durl=https://s01.oss.sonatype.org/service/local/staging/deploy/maven2/ \
 -DrepositoryId=sonatype
```


## 使用方式

maven 的 `settings.yml` 配置 sonatype 中央仓库：

```xml
<mirror>
    <id>mvnrepository</id>
    <mirrorOf>mvnrepository</mirrorOf>
    <url>http://mvnrepository.com/</url>
</mirror>

<mirror>
    <id>sonatype</id>
    <mirrorOf>sonatype</mirrorOf>
    <url>https://s01.oss.sonatype.org/</url>
</mirror>
```

项目的 `pom.xml` 配置构件坐标：

```xml
<dependency>
    <groupId>com.exp-blog</groupId>
    <artifactId>soapui</artifactId>
    <version>1.7.1</version>
</dependency>
```
