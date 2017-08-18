---
title: JS BOM DOM
date: 2017-08-25 17:28:44
tags: ["Js", "Front-end", "DOM"]
categories: ["Web","Front-end"]
description:
lang: zh-Hans
---
### DOM ###
DOM是W3C的标准。它允许程序和脚本动态地访问和更新文档的内容、结构和样式。
DOM分为三部分：核心DOM，XML DOM，HTML DOM
DOM基本操作包括：获取节点，节点操作，属性操作和文本操作。
HTML DOM的根节点是document

### 浏览器对象模型 (BOM) ###
javacsript是通过访问BOM（Browser Object Model）对象来访问、控制、修改客户端(浏览器)

BOM的核心是window，而window对象又具有双重角色，它既是通过js访问浏览器窗口的一个接口，又是一个Global（全局）对象。这意味着在网页中定义的任何对象，变量和函数，都以window作为其global对象

Window对象包含属性：document、location、navigator、screen、history、frames </br>
`navigator`对象：包含大量有关Web浏览器的信息，在检测浏览器及操作系统上非常有用，也可用window.navigator引用它：`.cookieEnabled` `.javaEnabled` `.userAgent`

还有`alert()` `focus()` `setTimeout()`等方法，都是BOM实现的
