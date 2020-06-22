# JavaScript 笔记

## JavaScript 基础

### Script 标签

- 在HTML文档中使用`Script`标签插入JavaScript程序;

    ```html
    <html>
        <body>
            <script>
                alert("Hi");
            </script>
        </body>
    </html>
    ```
    
### 外部脚本

- 通过`src`特性将JavaScript代码添加到HTML中;

    ```html
    <script src = "/path/to/script.js"></script>
    ```

一个单独的`<script>`不能同时使用`src`特性和内部包裹代码

## JavaScript 代码结构

### 语句

- 语句之间用分号进行分割,每条语句独占一行;

    ```javascript
    alert('Hello');
    alert('World');
    ```
    
### 注释

单行注释;

`//这是单行注释`

多行注释;

<pre>/*这是
多行注释
*/</pre>



## JavaScript 布局

- 通常JavaScript代码放在`<head> </head>`中;

    ```JavaScript
    <html>
        <head>
            <script type="text/JavaScript">
                alert('Hello, world');
            </script>
        </head>
        <body>
            ...
        </body>
    </html>
    ```

    > `type`默认属性为:`JavaScript`,不必显示指定。

- 将JavaScript代码单独放在`.js`文件中;

    ```JavaScript
    <html>
        <head>
            <script src="/static/js/abc.js"></script>
        </head>
        <body>
            ...
        </body>
    </html>
    ```
    
    > 多个页面可以同时引用一个`.js`文件
    
## JavaScript 基础
    
### 基本语法
    
JavaScript每个语句以`;`结尾,语句块用`{...}`
    
- 赋值语句;
    
    `var x = 1;`

- 一个字符串;

    `'Hello, world';`

- 代码包含两个语句,用`;`表示语句结束;

    `var x = 1; var y = 2;`

- 语句块是一组语句的集合,下面代码先做了一个判断,如判断成立,则执行`{...}`中所有语句;

    `if (2 > 1) {
        x = 1;
        y = 2;
        z = 3;
    }`

- `{...}`进行嵌套,形成层级结构;

    ```JavaScript
    if (2 > 1) {
        x = 1;
        y = 2;
        z = 3;
        if (x < y) {
        z = 4;
        }
        if (x > y) {
        z = 5;
        }
    }
    ```
    
- JavaScript注释;

    ```JavaScript
    //这是一行注释
    
    /*这
    是
    一块
    注释*/
    ```
    
### 数据类型和变量
    
#### Number

- JavaScript不区分浮点数和整数,统一用Number表示;
    
    ```JavaScript
    123; // 整数
    0.456; // 浮点数
    1.2345e3; // 科学计数法表示1.2345x1000,等同于1234.5
    -99; // 负数
    NaN; // NaN表示Not a Number,当无法计算时用NaN表示
    Infinity; // Infinity表示无限大,数值超过JavaScript的Number最大值时,表示为Infinity
    ```
    
- JavaScript四则运算

    ```JavaScript
    1 + 2; // 3
    (1 + 2) * 5 / 2; // 7.5
    2 / 0; // Infinity
    0 / 0; // NaN
    10 % 3; // 1
    ```
#### 字符串

字符串是以`'`或`""`括起来的任意文本,比如`'abc'`,`"efg"`

#### 布尔值

- 一个布尔值只有`true`、`false`两种值

    ```JavaScript
    true; // true值
    false; // false值
    2 > 1; // true值
    2 >= 3; // false值
    ```

- `&&`运算是与运算,只有都为`true`,结果才能是`true`

    ```JavaScript
    true && true; // 计算结果为true
    true && false; // 计算结果为false
    false && true && true // 计算结果为false
    ```
    
- `||`运算是或运算,只要其中一个为`true`,运算结果为`true`

    ```JavaScript
    false || false; //计算结果为false
    false || true; // 计算结果为true
    false || false || true; //计算结果为true
    ```
    
- `!`运算是非运算,它是一个单目运算符,把`true`变成`false`,把`false`变成`true`

    ```JavaScript
    ! true; // 结果为false
    ! false; // 结果为true
    ```
    
- 布尔值用在条件判断中
    
    ```JavaScript
    var age = 15;
    if (age >= 18) {
        alert('adult');
    } else {
        alert('teenager');
    }
    ```
    
#### 比较运算符

- `==`比较会自动转换数据类型再比较

    ```JavaScript
    false == 0; // true
    2 > 5; // false
    7 == 7; // true
    ```
    
- `===`比较不会自动转换数据类型,如不一致返回`false`,如一致再比较

    ```JavaScript
    false === 0; // false
    1 + 2 === 4 - 1; // true
    ```
    
- `NaN`与其他值都不相等,包括自己,只有`isNaN()`函数能判断`NaN`

    ```JavaScript
    NaN === NaN; // false
    isNaN(NaN); //不确定*不是Number所有返回true
    ```

- 浮点数相等比较

    ```javaScript
    1 / 3 === (1 - 2 / 3); // false
    ```


#### 数组

- 数组是一组按顺序排列的集合,集合的每个值为元素

    ```JavaScript
    [1, 2, 3.14, 'Hello', null,true];
    ```
