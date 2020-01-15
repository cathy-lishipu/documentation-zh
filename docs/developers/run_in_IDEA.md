# 使用IDEA运行我们的节点（针对当前master分支）

## 配置集成开发环境IDEA
**请确保IDEA已经完成如下配置**
- Oracle JDK 1.8（当前不支持OpenJDK）
- 安装Lombok插件

![](../../imags/lombok.png)

- 将Compiler下Annotation Processors中的Enable annotation processing前打勾

![](../../imags/annotation.png)

## 部署指南
**创建目录**
_/deploy/java-tron_

**克隆最新的代码https:github.com/tronprotocol/java-tron 到上述目录**
```swift
git clone https://github.com/tronprotocol/java-tron java-tron/
```

**切换master分支**
```swift
git checkout -t origin/master
```

**编译代码**
- 若编译test类
```swift
./gradlew build
```

编译成功，你可以看到类似如下块信息：

![](../../imags/build_success_test.png)

- 若不编译test类
```swift
./gradlew build -x test
```

编译成功，你可以看到类似如下块信息：

![](../../imags/build_success_notest.png)

**启动程序**

![](../../imags/start.png)

启动后可查看日志验证是否启动成功，日志路径为：/deploy/java-tron/tron/logs/tron.log。
使用tail -f /logs/tron.log/命令来查看块同步日志。
若启动成功，你可以看到类似如下块同步的日志信息：

![](../../imags/start_success.png)
