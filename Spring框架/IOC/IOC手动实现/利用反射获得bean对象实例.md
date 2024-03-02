**利用反射获得bean对象实例**

&nbsp;

在解析完成后

**&#49;.利用反射获得对象实例**

Class cls = Class.forName(classFullPath);

Monster instance = (Monster)cls.newInstance();

**&#50;.通过set方法设置信息**

instance.setMonsterId(monsterId);

.

.

.

**&#51;.将完整的对象放入到ioc容器中**

ioc.put(id,instance);
