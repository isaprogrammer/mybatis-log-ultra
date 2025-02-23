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

`在运行的本地项目中提取完整的SQL语句还是太繁琐了，需要配置、拼接，如果日志滚动的太快还难以定位，开发这款插件的目的，就是为了节省时间`

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

## 三、支持的场景

---

### 1、对单个接口进行拦截

- 自动拼接参数后输出到控制台，可以直接执行

<table>
    <tr>
        <td><img src="./picture/参数拼接完整，可直接执行.png" alt="参数拼接完整" width="240"></td>
        <td><img src="./picture/增强这个接口.png" alt="增强这个接口" width="240"></td>
        <td><img src="./picture/完整的SQL输出.png" alt="完整的SQL输出" width="240"></td>
    </tr>
</table>

---

### 2、支持@Mapper注解的接口方法

<table>
    <tr>
        <td><img src="./picture/带mapper注解的.jpg" width="240" alt=""></td>
    </tr>
</table>

---

### 3、如果你配置了mybatis log日志输出，默认也会替你进行拼接

---

## 四、功能规划中。。。

#### 1、可以将控制台输出切换为表格，提供更多的操作按钮，例如：格式化、复制、搜索..等等。

#### 2、远程环境也可以动态增强，输出完整的sql到文件

```shell
java -jar mybatis-log-ultra-agent.jar '${pid}' '${class}' '${method}'
```

#### 3、

