# demo
# 手写springboot简单项目

未使用idea自带的spring创建方法

## 开始

#### 1.打开idea创建project

#### 2.选择maven  --》 next

#### 3.输入GAV

输入GroupID（com.xxx）、ArtifactId(springbootDemo)、Version默认        GAV唯一确定一个jar包  整个项目就是一个包

#### 4.选择项目存放位置

#### 5.创建成功  附项目结构

 ![1562118608786](D:\Desktop\springboot_Demo\1562118608786.png)

pom.xml  内容

![1562118660536](D:\Desktop\springboot_Demo\1562118660536.png)

#### 	6. 添加maven依赖

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

#### 7.编写启动启动类

```java
@SpringBootApplication
public class Main {
    public static void main(String[] args) {
        SpringApplication.run(Main.class, args);
    }
}
```

