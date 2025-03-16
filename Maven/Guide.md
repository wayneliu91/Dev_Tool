# 常用镜像仓库地址

```xml
<mirror>
    <id>aliyunmaven</id>
    <mirrorOf>*</mirrorOf>
    <name>阿里云公共仓库</name>
    <url>https://maven.aliyun.com/repository/public</url>
</mirror>

<mirror>
    <id>huaweicloud</id>
    <mirrorOf>*</mirrorOf>
    <name>华为云公共仓库</name>
    <url>https://mirrors.huaweicloud.com/repository/maven/</url>
</mirror>

<mirror>
    <id>tencentcloud</id>
    <mirrorOf>*</mirrorOf>
    <name>腾讯云公共仓库</name>
    <url>https://mirrors.cloud.tencent.com/maven/</url>
</mirror>
```

# 下载依赖命令

## 基本命令
此命令的作用是解析并下载项目的所有依赖项到本地仓库，需在项目的根目录（包含pom.xml文件的目录）下执行`mvn dependency:resolve`命令。

## 只下载依赖，不执行其他构建操作
如果只想下载项目的依赖，而不执行编译、测试等其他构建操作，可以使用`mvn dependency:go-offline`命令。
此命令会解析项目的依赖，并确保所有依赖都已下载到本地仓库，以便后续在离线环境中使用。
