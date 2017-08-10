---
title: JS - DevNote - Target&CurrentTarger&This
date: 2017-08-10 11:46:30
tags: ["Js", "Front-end"]
categories: ["Web","Front-end"]
description:
lang: zh-Hans
---

在项目里为了实现button的拖拽时候，接触到了Target CurrentTarget，做了点小测试，终于是会用了，但总归耽误了不少时间，这里做点笔记，把各个关系理清楚。

首先得搞清楚JS的事件流的原理。

<!-- more -->
## JS 的事件流

参考 [Js 事件原理分析](http://www.cnblogs.com/st-leslie/p/5907556.html)

#### Bubbling vs Capturing

冒泡流是IE提出的，旧版并不支持捕获流。
总结下来，js事件从windows开始，到document->body->div...->element1->element0 <br>
这个过程称为捕获Capturing
随后对目标进行对应函数处理，这个过程是目标过程 <br>
最后再从element0返回window的过程则是冒泡 Bubbling。

``` javascript
      element0.onclick=function(){
        alert("element0_click");
      }
      element1.onclick=function(){
        alert("element1_click");
      }

```
所以依据冒泡次序，程序结果会先出现`element0_click` 再出现`element1_click `
#### DOM Level

DOM level 是W3C对DOM标准化的结果，目前到DOM Level 4
level0 和 level2 区别主要在于 level2支持了多事件binding
``` javascript
      element0.onclick=function(){
        alert("element0_click");
      }
      element0.onclick=function(){
        alert("element0_click2");
      }
      element1.onclick=function(){
        alert("element1_click");
      }
```  
level0会忽略前面的binding，只显示`element0_click2`最后`element1_click`

``` javascript
      element0.addEventListener("click",function(){
        alert("element0_click");
    },false);
      element0.addEventListener("click",function(){
        alert("element0_click2");
    },false);
      element1.addEventListener("click",function(){
        alert("element1_click");
    },false);
```
值得一提的是，`addEventListener`方法在IE中并不被支持，level2的对应实现是`attachEvent`
相对应的事件名则是`onclick`

#### *** stopPropagation() *** & *** preventDefault() ***
js的拖拽往往会用到  *** preventDefault() *** 这个函数取消事件的默认行为

``` javascript
        function dragStartHandler(e) {
           console.log('dragStartHandler');
           e.dataTransfer.setData('data', e.target.id);
       }
       function dragendHandler(e) {
           console.log('dragendHandler');
       }
       function dragoverHandler(e) {
           e.preventDefault();
       }
       function dropHandler(e) {
           e.preventDefault();
           var draggedID = e.dataTransfer.getData('data');
           var currentID = e.target.id;
           var draggedEle = document.getElementById(draggedID);
           var currentEle = document.getElementById(currentID);
          //...
       }
```
而  *** stopPropagation() *** 则阻止了事件进一步获取或冒泡，同时阻止任何事件处理程序被调用



<blockquote class="blockquote-center">
target在事件流的目标阶段；currentTarget在事件流的捕获，目标及冒泡阶段。只有当事件流处在目标阶段的时候，两个的指向才是一样的， 而当处于捕获和冒泡阶段的时候，target指向被单击的对象而currentTarget指向当前事件活动的对象(注册该事件的对象)（一般为父级）。this指向永远和currentTarget指向一致（只考虑this的普通函数调用）。
</blockquote>











END
