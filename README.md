<h2 align="center">mybatis-log-ultra</h2>

<p align="center">
	<strong>一切为了效率</strong>
</p>

<p align="center">
    <a href="http://www.apache.org/licenses/LICENSE-2.0.html" target="_blank">
        <img src="http://img.shields.io/:license-apache-brightgreen.svg" >
    </a>
    <a>
        <img src="https://img.shields.io/badge/JDK-1.8+-green.svg" >
    </a>
    <a>
        <img src="https://img.shields.io/badge/IDEA-2024.0+-green.svg" >
    </a>
</p>

### 一、简介

`在运行的本地项目中提取完整的SQL语句还是太繁琐了，需要配置、拼接，如果日志滚动的太快还难以定位，开发这款插件的目的，就是为了节省时间`

### 二、支持的场景

- 支持对单个接口内执行的SQL进行拦截，自动拼接参数后输出到控制台，可以直接执行

<img src="./picture/参数拼接完整，可直接执行.png" width="240" alt="">
<img src="./picture/增强这个接口.png" width="240" alt="">
<img src="./picture/完整的SQL输出.png" width="240" alt="">

- 支持拦截使用了@Mapper注解的接口方法
