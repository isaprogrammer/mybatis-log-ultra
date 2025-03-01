<h2 align="center">mybatis-log-ultra</h2>

<p align="center">
	<strong>为了高效，为了便捷</strong>
</p>

<p align="center">
    <a href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">
        <img src="http://img.shields.io/:license-apache-brightgreen.svg" >
    </a>
    <a>
        <img src="https://img.shields.io/badge/JDK-1.8+-green.svg" >
    </a>
    <a>
        <img src="https://img.shields.io/badge/IDEA-2023.0+-green.svg" >
    </a>
</p>

## 一、简介

`在运行的本地项目中提取完整的SQL语句还是太繁琐了，需要配置、拼接，如果日志滚动的太快还难以定位，开发这款插件的目的，就是为了节约点提取SQL的时间`

`为什么是mybatis log ultra？因为小米su7 ultra`

## 二、要求

<p>
    <a>
        <img src="https://img.shields.io/badge/JDK-1.8+-green.svg" >
    </a>
    <a>
        <img src="https://img.shields.io/badge/IDEA-2023.0+-green.svg" >
    </a>
    <a>
        <img src="https://img.shields.io/badge/Mybatis-必选-green.svg" >
    </a>
    <a>
        <img src="https://img.shields.io/badge/Spring-非必选-green.svg" >
    </a>
</p>

## 三、目前市面上已有插件未能解决的痛点问题

1、需要添加mybatis的配置

2、日志滚动太快，难以查找、难以选中

3、SQL和参数是单独打印，还需要手动进行拼接

4、只输出部分SQL需修改配置，还需要重启

## 四、操作手册

---

### 1、默认情况下，项目启动即自动拦截所有的@RestController注解的类
<table>
    <tr>
        <td><img src="./picture/增强@RestController注解的类.png" alt="增强@RestController注解的类" width="960"></td>
    </tr>
</table>

### 2、请求接口即可获取到完整可执行的SQL
<table>
    <tr>
        <td><img src="./picture/请求接口即可获取可执行SQL.png" alt="请求接口即可获取可执行SQL" width="960"></td>
    </tr>
</table>

### 3、快速的拷贝SQL语句
<table>
    <tr>
        <td><img src="./picture/复制SQL.jpg" alt="复制SQL" width="960"></td>
    </tr>
</table>

---

### 4、普通方法也是独立进行输出

<table>
    <tr>
        <td><img src="./picture/增强这个接口.png" width="960" alt=""></td>
    </tr>
</table>

---

### 5、@Mapper注解的接口也同样支持

<table>
    <tr>
        <td><img src="./picture/带mapper注解的.jpg" width="960" alt=""></td>
    </tr>
</table>

---

## 五、功能规划中。。。

#### 1、提供更多的快捷操作，例如：格式化、预览、复制、搜索..等等，尽可能在当前页面完成

#### 2、远程环境也可以动态增强，输出完整的sql到文件，类似是arthas的使用方式，让本地和远程拥有相似的体验

```shell
# 类似这样的命令
java -jar mybatis-log-ultra-boot.jar '${pid}' '${class}' '${method}'
```

#### 3、打印mybatis log只是一个开始，下个支持的组件大概率是Elasticsearch

## 六、一个粗糙的开始，就是好的开始

