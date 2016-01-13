##Gradle Wrapper

GradleWrapper主要作用是两个：

1. 发布到网络上的代码如果要被下载者成功构建，那么下载者需要自己去下载，安装，配置Gradle，浪费太多时间。
2. 团队开发中大家最好都使用同一个Gradle版本来构建项目

###为项目添加Wrapper

只需要在项目根目录下面执行：

		gradle wrapper --gradle-version 2.2
		
当然，Wrapper的参数不一定需要在命令行里面指定，wrapper作为一个task，我们也可以使用build.gradle进行配置。

		task wrapper(type: Wrapper) {
			gradleVersion = '2.0'
		}

