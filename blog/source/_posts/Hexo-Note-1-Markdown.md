---
title: Hexo Note (1) - Markdown
date: 2017-08-02 11:29:03
tags: ["Hexo", "MD", "Web Log"]
categories: ["Hexo"]
description:
---
[Markdown Intro](http://www.jianshu.com/p/q81RER)

#### How to make refered words centered
```
<blockquote class="blockquote-center">Refered words
```
{% blockquote Lu, Lu's thoughts https://www.google.com %}
content
{% endblockquote %}
#### How to count visitors
```
<div class="ds-recent-visitors" data-num-items="39" data-avatar-size="40" id="ds-recent-visitors"></div>
```
<!-- more -->
#### Configure where "read more..." starts
` <!-- more --> `
#### Mouse click heart action
```
<script type="text/javascript" src="/js/src/love.js"></script>
```
#### Background
```
<script type="text/javascript" src="/js/src/particle.js"></script>
```
### Video

{% youtube video_id %}

#### Location
 `\themes\next\layout\_layout.swing`<br>
 `\themes\next\layout\_partials\header.swig`<br>
 `\themes\next\source\js\src`<br>
`themes\next\source\css\_custom\custom.styl`<br>
