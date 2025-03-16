# 配置

1、配置`GRADLE_HOME`环境变量，以便能在任何路径都能使用gradle命令。

2、配置`GRADLE_USER_HOME`环境变量，以便设置库的存放路径。
`GRADLE_USER_HOME=D:\Dev\config\.gradle`

3、设置镜像仓库地址
使用`Groovy DSL`配置，在`GRADLE_USER_HOME`路径下创建`init.gradle`文件。
```groovy
allprojects {
    repositories {
        // 添加阿里云 Maven 仓库
        maven { url 'https://maven.aliyun.com/repository/public' }
        // 添加 Maven 中央仓库
        mavenCentral()
    }
}
```

若你更喜欢使用`Kotlin DSL`，可以将文件重命名为`init.gradle.kts`，并添加以下内容：
```kotlin
allprojects {
    repositories {
        // 添加阿里云 Maven 仓库
        maven("https://maven.aliyun.com/repository/public")
        // 添加 Maven 中央仓库
        mavenCentral()
    }
}
```