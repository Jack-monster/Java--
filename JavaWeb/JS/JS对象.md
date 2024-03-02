# <center>JavaScript对象</center>

***
### 一、JavaScript创建对象的方式
- Object形式创建对象
- {}形式创建对象
### 二、Object形式创建对象
1. 对象的定义
	```javascript
	var objectName = new Object();//创建一个空的对象实例
	objectName.propertyName = value;//为对象定义一个属性
	objectName.methodName = function(){}//为对象定义一个方法
	```
2. 对象访问
	```javascript
	var variable = objectName.propertyName//访问对象属性
	object.methodName();//调用对象方法
	```
### 三、{}形式定义对象
1. 对象的定义
   ```javascript
   var objectName = {
	propertyName1 : value,//定义属性
	propertyName2 : value,//定义属性，注意有逗号
	methodName : function(){}//定义方法
   };
   ```
2. 对象访问
   ```javascript
	var variable = objectName.propertyName//访问对象属性
	object.methodName();//调用对象方法
   ```