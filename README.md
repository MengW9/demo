# demo
# 手写springboot简单项目

使用简单手写导包实现spring boot，未使用idea自带的spring创建方法

可以更加简单理解springboot启动过程 

## 开始

#### 1.打开idea创建project

![开始](.\img\1.png)

#### 2.选择maven  --》 next

![](.\img\2.png)

#### 3.输入GAV

输入GroupID（com.xxx）、ArtifactId(springbootDemo)、Version默认        GAV唯一确定一个jar包  整个项目就是一个包

![](.\img\3.png)

#### 4.选择项目存放位置

![](.\img\4.png)

#### 5.创建成功  

![](.\img\5.png)

#### 6.附项目结构

![](.\img\6.png)

#### 7. 添加maven依赖

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
  <dependency>				    		     	         
    <groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
  </dependency> 
</dependencies>

```

![](.\img\7.png)

#### 8.编写启动启动类

```java
@SpringBootApplication
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```

![](.\img\8.png)

#### 8.成功

![](.\img\9.png)

![](.\img\10.png)
