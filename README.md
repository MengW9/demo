# demo
# 手写springboot简单项目

使用简单手写导包实现spring boot，未使用idea自带的spring创建方法

可以更加简单理解springboot启动过程 

## 开始

#### 1.打开idea创建project

![开始](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828165218124-637115730.png)

#### 2.选择maven  --》 next

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828165258515-1753505230.png)

#### 3.输入GAV

输入GroupID（com.xxx）、ArtifactId(springbootDemo)、Version默认        GAV唯一确定一个jar包  整个项目就是一个包

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828165335280-1418674942.png)

#### 4.选择项目存放位置

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828165401206-2026618201.png)

#### 5.创建成功  

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828165431267-1020863951.png)

#### 6.附项目结构

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828165551327-759056223.png)

#### 7. 添加maven依赖

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828165703755-323065740.png)

```xml
<dependencyManagement>
    <dependencies>
        <!--spring 版本管理-->
        <dependency>
			<groupId>io.spring.platform</groupId>
            <artifactId>platform-bom</artifactId>
            <version>Cairo-SR8</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>

<dependencies>
  <!--spring web配置-->
  <dependency>				    		     	         <groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
  </dependency> 
</dependencies>

```

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828172645348-1183999254.png)

#### 8.编写启动启动类

```java
@SpringBootApplication
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828172645348-1183999254.png)

#### 8.成功

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828172727959-752339365.png)

![](https://img2018.cnblogs.com/blog/1697474/201908/1697474-20190828172745479-1016330239.png)
