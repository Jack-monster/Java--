**JS变量**

&nbsp;

**JS变量**

* **JavaScript声明的变量是弱类型的**

| var number = 12; window.alert(typeof number);//显示为number number = '12'; window.alert(typeof number);//显示为string |
| --- |


* **声明变量用var，变量的标识符是大小写敏感的**
* **声明块作用域变量可以用let、块作用域常量用const**
* **若声明变量却不赋值，它的值将是undefined**

| var carName; console.log(carName);//显示为undefined |
| --- |


* **JavaScript 变量赋值后再次声明却不赋值不会改变原来的值**

| var carName = "BMW"; console.log(carName);//BMW var carName; console.log(carName);//BMW |
| --- |

