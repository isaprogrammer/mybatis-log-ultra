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
        <td><img src="./picture/带mapper注解的.jpg" width="480" alt=""></td>
    </tr>
</table>

---

### 3、普通方法也是可以进行拦截的（排除了java.,javax......等一些工具类的增强）

---

### 4、如果你配置了mybatis log日志输出，默认也会替你进行拼接

---

### 5、快速复制SQL到粘贴板（无需拖拽选中，直接右键即可）

<table>
    <tr>
        <td><img src="./picture/复制SQL.jpg" width="480" alt=""></td>
    </tr>
</table>

---

## 四、一些思考（可能我的脑回路比较闭塞，望指正！🙏🙏🙏🙏🙏）

`大部分项目可能已经配置的mybatis log，sql和参数会输出在日志里，所以默认插件是不加载agent的，会直接从日志里提取出sql和参数进行拼接，并输出到**#.**的tab里，这是自己重新实现了类似mybatis log plus这类插件的功能，减少了一些bug，例如：同一个sql连续多次输出，sql和参数可能会匹配错乱的问题；SQL中包含DATE_FORMAT(?,'%Y-%m-%d %H:%i:%S')就会无法替换，因为他们将?换成了%s，然后%S又会有干扰`

`如果只有一个Tab展示所有SQL，SQL可能会滚动的太快，所以我干脆给你选中的每个接口都创建了一个Tab，但这样是欠考虑了，Tab太多了，感谢第一个提issue的大佬给我指出了一点，接下来我会把选中的接口合并到一个Tab里面去，或者找到更好的交互`

`还有一个很重要的体验是，如何快速的将SQL复制到粘贴板（复制到粘贴板的功能已经实现了，右键有个Mybatis Log Copy的选项），或者打开一个编辑页面，将SQL进行格式化，快速的预览。`

`大家如果有更好的建议，欢迎留下您的足迹🦶，👏👏👏👏👏👏`

`这是一个shi一般`

## 五、功能规划中。。。

#### 1、提供更多的快捷操作，例如：格式化、预览、复制、搜索..等等，尽可能在当前页面完成

#### 2、远程环境也可以动态增强，输出完整的sql到文件，类似是arthas的使用方式，让本地和远程拥有相似的体验

```shell
# 类似这样的命令
java -jar mybatis-log-ultra-boot.jar '${pid}' '${class}' '${method}'
```

#### 3、打印mybatis log只是一个开始，下个支持的组件大概率是Elasticsearch

## 六、一个粗糙的开始，就是好的开始

