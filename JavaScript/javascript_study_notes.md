# JavaScript 笔记

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
    
JavaScript每个语句以`;`结尾,语句块用`{...}`:
    
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
