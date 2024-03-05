# XML
## 为什么需要XML
1. 两个程序进行数据通信可以用XML
2. 服务器的初始配置文件可以用XML
3. XML可以存储复杂的数据关系
***
## 例子
1. Spring的IOC配置文件，beans.xml
2. mybatis的XXXMapper.xml
3. Tomcat的server.xml  web.xml
4. Maven的pom.xml
### XML文件示例
```xml
<?xml version="1.0" encoding="UTF-8" ?>
<students>
    <student id="100">
        <name>jack</name>
        <age>18</age>
        <gender>男</gender>
    </student>
</students>
```
同理xml文件也可以映射成一个