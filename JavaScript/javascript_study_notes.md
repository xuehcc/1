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
    
    JavaScript每个语句以`;`结尾,语句块用`{...}`
    
    赋值语句:
    ```JavaScript
    var x = 1;
    ```
    
    
