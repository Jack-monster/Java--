**@Target**

&nbsp;

[**@Target(ElementType.。。)**](<mailto:@Target(ElementType.。。)>)

**用于修饰Annotation定义，用于指定被修饰的Annotation能用于修饰哪些程序元素。**

@Documented\
@Retention(RetentionPolicy.*RUNTIME*)\
@Target(ElementType.*ANNOTATION\_TYPE*)\
public @interface Target {\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Returns an array of the kinds of elements an annotation
type*\
*&nbsp;&nbsp; &nbsp; \* can be applied to.*\
*&nbsp;&nbsp; &nbsp; \* **@return** an array of the kinds of elements an
annotation type*\
*&nbsp;&nbsp; &nbsp; \* can be applied to*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; ElementType\[\] value();\
}

&nbsp;

**@Target 也包含一个名为value的成员变量（ElementType数组）**

public enum ElementType {\
&nbsp; &nbsp; */\*\* Class, interface (including annotation type), or enum
declaration \*/*\
*&nbsp; &nbsp; TYPE*,\
\
&nbsp; &nbsp; */\*\* Field declaration (includes enum constants) \*/*\
*&nbsp; &nbsp; FIELD*,\
\
&nbsp; &nbsp; */\*\* Method declaration \*/*\
*&nbsp; &nbsp; METHOD*,\
\
&nbsp; &nbsp; */\*\* Formal parameter declaration \*/*\
*&nbsp; &nbsp; PARAMETER*,\
\
&nbsp; &nbsp; */\*\* Constructor declaration \*/*\
*&nbsp; &nbsp; CONSTRUCTOR*,\
\
&nbsp; &nbsp; */\*\* Local variable declaration \*/*\
*&nbsp; &nbsp; LOCAL\_VARIABLE*,\
\
&nbsp; &nbsp; */\*\* Annotation type declaration \*/*\
*&nbsp; &nbsp; ANNOTATION\_TYPE*,\
\
&nbsp; &nbsp; */\*\* Package declaration \*/*\
*&nbsp; &nbsp; PACKAGE*,\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Type parameter declaration*\
*&nbsp;&nbsp; &nbsp; \**\
*&nbsp;&nbsp; &nbsp; \* **@since** 1.8*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp; &nbsp; TYPE\_PARAMETER*,\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Use of a type*\
*&nbsp;&nbsp; &nbsp; \**\
*&nbsp;&nbsp; &nbsp; \* **@since** 1.8*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp; &nbsp; TYPE\_USE*\
}
