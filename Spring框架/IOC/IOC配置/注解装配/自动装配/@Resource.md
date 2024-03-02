**@Resource**

&nbsp;

**@Resource规则说明：**

1. **@Resource 有两个属性分别是name和type,Spring将@Resource注解的**

**name属性解析为bean的名字，而type属性解析为bean的类型。所以如果使用name属性**

**,则使用byName的自动注入策略（查找id为Name的组件），而使用type属性时则使用byType的自动注入策略**

@Target({*TYPE*, *FIELD*, *METHOD*})\
@Retention(*RUNTIME*)\
public @interface Resource {\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* The JNDI name of the resource.&nbsp; For field
annotations,*\
*&nbsp;&nbsp; &nbsp; \* the default is the field name.&nbsp; For method
annotations,*\
*&nbsp;&nbsp; &nbsp; \* the default is the JavaBeans property name
corresponding*\
*&nbsp;&nbsp; &nbsp; \* to the method.&nbsp; For class annotations, there is no
default*\
*&nbsp;&nbsp; &nbsp; \* and this must be specified.*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; String name() default "";\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* The name of the resource that the reference points to.
It can*\
*&nbsp;&nbsp; &nbsp; \* link to any compatible resource using the global JNDI
names.*\
*&nbsp;&nbsp; &nbsp; \**\
*&nbsp;&nbsp; &nbsp; \* **@since** Common Annotations 1.1*\
*&nbsp;&nbsp; &nbsp; \*/*\
\
*&nbsp;* &nbsp; String lookup() default "";\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* The Java type of the resource.&nbsp; For field
annotations,*\
*&nbsp;&nbsp; &nbsp; \* the default is the type of the field.&nbsp; For method
annotations,*\
*&nbsp;&nbsp; &nbsp; \* the default is the type of the JavaBeans property.*\
*&nbsp;&nbsp; &nbsp; \* For class annotations, there is no default and this must
be*\
*&nbsp;&nbsp; &nbsp; \* specified.*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; Class\<?\> type() default java.lang.Object.class;\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* The two possible authentication types for a resource.*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; enum AuthenticationType {\
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; *CONTAINER*,\
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; *APPLICATION*\
*&nbsp;* &nbsp; }\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* The authentication type to use for this resource.*\
*&nbsp;&nbsp; &nbsp; \* This may be specified for resources representing a*\
*&nbsp;&nbsp; &nbsp; \* connection factory of any supported type, and must*\
*&nbsp;&nbsp; &nbsp; \* not be specified for resources of other types.*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; AuthenticationType authenticationType() default
AuthenticationType.*CONTAINER*;\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Indicates whether this resource can be shared between*\
*&nbsp;&nbsp; &nbsp; \* this component and other components.*\
*&nbsp;&nbsp; &nbsp; \* This may be specified for resources representing a*\
*&nbsp;&nbsp; &nbsp; \* connection factory of any supported type, and must*\
*&nbsp;&nbsp; &nbsp; \* not be specified for resources of other types.*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; boolean shareable() default true;\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* A product specific name that this resource should be
mapped to.*\
*&nbsp;&nbsp; &nbsp; \* The name of this resource, as defined by the
\<code\>name\</code\>*\
*&nbsp;&nbsp; &nbsp; \* element or defaulted, is a name that is local to the
application*\
*&nbsp;&nbsp; &nbsp; \* component using the resource.&nbsp; (It's a name in the
JNDI*\
*&nbsp;&nbsp; &nbsp; \* \<code\>java:comp/env\</code\> namespace.)&nbsp; Many
application servers*\
*&nbsp;&nbsp; &nbsp; \* provide a way to map these local names to names of
resources*\
*&nbsp;&nbsp; &nbsp; \* known to the application server.&nbsp; This mapped name
is often a*\
*&nbsp;&nbsp; &nbsp; \* \<i\>global\</i\> JNDI name, but may be a name of any
form. \<p\>*\
*&nbsp;&nbsp; &nbsp; \**\
*&nbsp;&nbsp; &nbsp; \* Application servers are not required to support any
particular*\
*&nbsp;&nbsp; &nbsp; \* form or type of mapped name, nor the ability to use
mapped names.*\
*&nbsp;&nbsp; &nbsp; \* The mapped name is product-dependent and often
installation-dependent.*\
*&nbsp;&nbsp; &nbsp; \* No use of a mapped name is portable.*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; String mappedName() default "";\
\
&nbsp; &nbsp; */\*\**\
*&nbsp;&nbsp; &nbsp; \* Description of this resource.&nbsp; The description is
expected*\
*&nbsp;&nbsp; &nbsp; \* to be in the default language of the system on which
the*\
*&nbsp;&nbsp; &nbsp; \* application is deployed.&nbsp; The description can be
presented*\
*&nbsp;&nbsp; &nbsp; \* to the Deployer to help in choosing the correct
resource.*\
*&nbsp;&nbsp; &nbsp; \*/*\
*&nbsp;* &nbsp; String description() default "";\
}

&nbsp;

2. **如果@Resource没有指定name和type，则先使用byName注入策略，如果匹配不上，再使用**

**byType策略，如果都不成功，就会报错**
