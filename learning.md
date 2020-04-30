### less(css预处理编辑器)
1、vscode 下载 easy less 插件

2、在设置中设置处理输出类型
```
"less.compile": {
    "outExt": ".css"   // 输出文件类型 /.wxss
}
```
#### 注释
1. 双斜杠(//) 注释只会在 less 文件中显示，在编译后的 css 文件中看不到注释内容
2. (/* */) 注释在 less 和 css 文件中都能看到注释内容

#### 变量(variables)

#### 混合(mixins)
```
.color(@c){     // 相当于函数定义 传参
    color: @c；
    border：1px solid @c;
}
// 使用
.boot{
    width: 100px;
    height: 100px;
    .color(green)  // 出入传入参数调用
}
```
#### 嵌套规则(nested-rules)
**&：代表当前的选择器**
```
@color: red;
@active-color: blue;
@width: 100px;
@height: 100px;
div{
    width: @width;
    height: @height;
    ul{
        list-style: none;
    }
    li{
        display: block;
        height: 50px;
        width: 50px;
        border: 1px solid @color;
        a{
            text-decoration: none;
            color: @color;
            &:hover{
                color: @active-color;
            }
        }
    }
}
```

#### 运算(operations)

#### 函数(functions)

#### 命名空间

#### 作用域

#### 