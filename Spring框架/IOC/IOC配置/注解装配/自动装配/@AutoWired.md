**@AutoWired**

&nbsp;

**@AutoWired规则说明：**

1. **先在IOC容器中查找待装配的组件的类型，如果有唯一的bean匹配，则使用该bean装配**
1. **如待装配的类型对应的bean在IOC容器中有多个，则使用待装配的属性的属性名作为id值再进行查找，找到则装配，找不到会抛出异常**
