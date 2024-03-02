**@Retention**

&nbsp;

[**@Retention(RetentionPolicy.\*)**](<mailto:@Target(ElementType.。。)>)

**说明**

**只能用于修饰一个Annotation定义，用于指定该Annotation可以保留多长时间类型的成员变量，使用@Retention时必须为该value成员变量指定值：**

@Documented\
@Retention(RetentionPolicy.*RUNTIME*)\
@Target(ElementType.*ANNOTATION\_TYPE*)\
public @interface Retention {\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Returns the retention policy.*\
*&nbsp;&nbsp; &nbsp; \* **@return** the retention policy*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; RetentionPolicy value();\
}

&nbsp;

**RetentionPolicy **

public enum RetentionPolicy {\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Annotations are to be discarded by the
compiler.编译器执行后丢弃*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp; &nbsp; SOURCE*,\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Annotations are to be recorded in the class file by the
compiler*\
*&nbsp;&nbsp; &nbsp; \* but need not be retained by the VM at run time.&nbsp;
This is the default*\
*&nbsp;&nbsp; &nbsp; \* behavior.*

*&nbsp;\* 注解将被编译器记录于字节码文件中，但不被JVM所保留。如果不加入Retention注释*

*&nbsp;\* 默认的annotation都是按此方法来保留*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp; &nbsp; CLASS*,\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Annotations are to be recorded in the class file by the
compiler and*\
*&nbsp;&nbsp; &nbsp; \* retained by the VM at run time, so they may be read
reflectively.*\
*&nbsp;&nbsp; &nbsp; \*注解不仅会被编译器记录于字节码文件中，还会在VM虚拟机中保留，因而可以被反射性的读取主要的注&nbsp;
&nbsp; &nbsp; \* 解*\
*&nbsp;&nbsp; &nbsp; \* **@see** java.lang.reflect.AnnotatedElement*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp; &nbsp; RUNTIME*\
}
