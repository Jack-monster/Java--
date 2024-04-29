# 常量与变量 
## 初始化变量
==**java中声明一个变量后，必须用赋值语句显式地初始化变量**==

```java
    String hello;
    System.out.print(hello);//error！！

    String hello = "hello";
    System.out.print(hello);//Correct!
```
## 简化声明变量 
Java10后,如果可以从变量初始值推断出其类型，就不需要声明类型。只需要使用var关键字。

```java
    var day = 1;//自动推断出day为int
    var greeting = "hello";//推断出greeting 为String
```

## 枚举类型
有时候需要表示一些变量，其值只有有限多个。例如衣服的尺寸，一年的四季。这时候可以自定义枚举类型。
```java
    enum Size {SMALL,MEDIUM,LARGE,EXTRA_LARGE};//定义有四种值的枚举类型Size
    Size s = Size.MEDIUM;//声明一个枚举类型
```
枚举类型的变量只能存储类型声明中所列的某个值，或特殊值null，null表示这个变量没有设置任何值。