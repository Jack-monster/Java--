# <center>JavaScript事件</center>
***
<font size=4>Javascript通过与HTML元素绑定而完成事件响应的一种语言</font>
***
## 常见的HTML元素
| 事件 | 描述 |
| :----- | --------: |
| onchange | HTML元素已被改变|
| onclick | HTML元素被点击 |
| onmouseover | 把鼠标移动到HTML元素上|
|onmouseout | 把鼠标移开HTML元素|
|onkeydown | 按下键盘按键 |
| onload | 浏览器加载完页面 |
***
## 事件绑定的分类
1. **静态注册事件**
   通过html标签的事件属性直接赋予事件响应后的代码
   ```html
    <button onclick="document.getElementById('myImage').src='./img/turnOn.gif'">开灯</button> 
   ```
2. **动态注册事件**
   通过js代码获取***dom***对象，，通过`dom对象.事件名 = function(){}`的形式称为动态注册
3. **实例**
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
      <meta charset="UTF-8">
      <title>jsLearningHTML</title>
      <script type="text/javascript">
         function sayOk () {
               alert("Ok")
         }
         window.onload = function () {//这段代码将在页面加载结束后执行，是动态绑定
            let button1 = document.getElementById("answer");
            button1.onclick = function () {
                alert("you've clicked the button")
            }
         }
      </script>
   </head>
   <body>
   <h1>js函数测试</h1>
   <button onclick="sayOk()">静态</button>
   <button id="answer">动态</button>
   </body>
   </html>
   ```
***
# onsubmit事件
***
###一、静态注册示例

<h2>用户注册</h2>
<form action="ok.html" autocomplete="on" onsubmit="return register()" target="_blank">
    u: <input type="text" name="username" id="username"><br/>
    p: <input type="password" name="pwd" id="pwd"><br/>
    <input type="submit" value="注册用户">
</form>

1. ```html
      html代码
      <form action="ok.html" autocomplete="on" onsubmit="return register()" target="_blank">
      u: <input type="text" name="username" id="username"><br/>
      p: <input type="password" name="pwd" id="pwd"><br/>
      <input type="submit" value="注册用户">
      </form>
   ```
2. ```javascript
      javascript代码
      function register() {
            let username = document.getElementById("username");
            let pwd = document.getElementById("pwd");
            if (username.value === ""|| pwd.value === "" ) {
                alert("请填写完整信息")
                return false
            }
            return true
        }
   ```
- **form**标签的 onsubmit属性通过使用`onsubmit="return register()"`来获得register函数的返回值<br/>这样当表单内容不完整时就不会提交执行action
***
###二、动态注册示例