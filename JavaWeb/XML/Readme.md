# XML学习笔记
[TOC]
## 1.为什么需要XML
1. 两个程序进行数据通信可以用XML
2. 服务器的初始配置文件可以用XML
3. XML可以存储复杂的数据关系
***
## 2.例子
1. Spring的IOC配置文件，beans.xml
2. mybatis的XXXMapper.xml
3. Tomcat的server.xml  web.xml
4. Maven的pom.xml
***
## 3.XML文件示例
```xml
<?xml version="1.0" encoding="UTF-8" ?>//文档说明
<students>
    <student id="100">
        <name>jack</name>
        <age>18</age>
        <gender>男</gender>
    </student>
</students>
```
同理xml文件也可以映射成一个DOM
***
## 4.XML文件的构成
1. 文档声明
2. 元素
3. 属性
4. 注释
5. CDATA区，特殊字符
### 4.1 文档声明
1. 文档声明应放在XML文档的第一行
### 4.2 元素
1. 每个XML文档必须有且只有一个根元素
2. 元素命名是区分大小写的、不包含空格、不以数字开头、且不能包含冒号
### 4.3 属性
1. 属性是写在元素标签内的键值对
2. 每个元素不能有多个重复的属性
3. 属性名称区分大小写
### 4.4 CDATA节
用CDATA节包含的文本不会被XML解析引擎解析，而是当做普通文本内容
```
    <![CDATA[
    在这里键入你的文本
    ]]>
```
***
## 5. DOM4J--XML解析技术
### 5.1 解析原理
1. 不管是html文件还是xml文件都是标记型文档，都可以使用w3c组织制定的dom技术来解析
2. 将文档映射成dom对象后可以通过java技术对dom对象进行相关操作