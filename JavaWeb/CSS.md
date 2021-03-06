CSS编程语言【简单了解】
就是一个提升代码复用性的东西
[TOC]
# 一.介绍:
1. 是一种专门在浏览器编译并执行的编程语言.
2. 用于定位浏览器中HTML标签并对定位的HTML标签中【样式属性】进行统一管理
# 二.HTML标签属性分类
1. 基本属性:
大多数HTML标签都拥有属性,是一个非常庞大群体
比如id属性,相当于身份证编号,用于区分HTML标签
`<input type="text" id="one"/>`
`<input type="text" id="two"/>`
比如 name属性,相当于人名字,允许一组标签拥有相同name
`<input type="text" id="one"  name="myText"/>`
`<input type="text" id="two"  name="myText"/>`
2. 样式属性:
是一个非常庞大群体,通知浏览器将HTML标签中数据在浏览器中以指定形态展示
`<div style="background-color:red;color:green;width:300px;height:200px"></div>`
div动态图层
3. 工作状态属性:
只存在于【表单域标签】中,用于表示【表单域标签】状态.
checked:存在于radio与checkbox中,表示标签是否被选中
disabled:表示标签处于不可用状态
readOny:表示标签处于只读状态
seleteced:存在option标签,表示标签是否被选中
4. 监听属性:
监听属性用户与HTML标签之间进行通信通道,监听属性用于监听用户在何时对当前标签进行何种操作,当指定操作产生时,监听属性将会通知浏览器调用对应JavaScript方法处理当前请求
onmouseover,当发生行为,调用js
# 三.样式属性开发难度:
1. 由于网页经常出现大量的HTML标签拥有相同的样式属性设置,因此导致
前端工程师进行大量重复性开发操作.
2. 当用户修改需求时,导致前端工程师进行大量重复维护工作
ibelee: 所以就是一个在样式属性上提高代码复用度的东西
# 四.CSS编程语言作用:
1. 通知浏览器将所有满足定位条件的HTML标签进行统一定位
2. 通知浏览器对已经定位HTML标签中样式属性进行集中统一赋值管理
把所有的style在head中统一管理
# 五.CSS选择器:
1. 介绍:
CSS选择器,实际上就是一组定位条件用于定位HTML标签.
CSS选择器有9个大的分类
2. CSS选择器语法格式:
```
<html>
    <head>
        <!--type='text/css',-->
        <style type="text/css">
            定位条件{
            "样式属性1":"值1";
            "样式属性2":"值2"
            }
        </style>
    </head>
</html>
```
# 六.ID选择器:
1. 介绍:
根据HTML标签中ID属性的值进行定位
都要写在head中
2. 语法:
```
<style type="text/css">
    #id编号{
    "样式属性1":"值1";
    "样式属性2":"值2"
    }
</style>
```
# 七.标签类型选择器:
1. 介绍:
根据HTML标签类型进行定位
例如对所有的div/p进行操作
2. 语法:
```
<style type="text/css">
标签类型名{
"样式属性1":"值1";
"样式属性2":"值2"
}
</style>
```
# 八.层级选择器
1. HTML标签之间关系:
父子关系
兄弟关系
2. 父子关系:
即为包含关系
```
<tr>
    <td>
        <input type="text">
    </td>
</tr>
```
td标签是tr标签的子标签
input标签是td标签的子标签
3. 兄弟关系:
一组标签拥有相同的父标签,并且彼此之间
没有任何包含关系,即为兄弟
```
<body>
    <div>1</div>  大哥
    <p>2</p>      二哥
    <span>3</span> 三弟
</body>
```
4. 层级选择器介绍:
根据标签之间父子关系或则兄弟关系进行定位
5. 简单的层级选择器
```
<style type="text/css">
    定位父标签条件  定位子标签条件{
        "样式属性1":"值1";
        "样式属性2":"值2"
      }
        找到指定父标签下满足条件的所有子标签
</style>
```
# 九.自定义选择器
1. 介绍:
如果一组HTML标签之间没有相同的特征,但是却需要对指定属性赋值相同内容,此时将自定义选择器绑定到对应标签上
2. 语法:
```
<style type="text/css">
.自定义选择器名{
color:red;
}
</style>
<div class="自定义选择器名"></div>
<p   class="自定义选择器名"></p>
```