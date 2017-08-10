---
title: Hexo Note (2) - Advance
date: 2017-08-10 10:29:03
tags: ["Hexo", "Web"]
categories: ["Web","Hexo"]
description:
lang: zh-Hans
---

### Import Douban Homepage
``` html
{% raw %}
<div id="life">
<h1 style="text-align: center">我看过的电影和书籍<h1>
<script type="text/javascript" src="http://www.douban.com/service/badge/User_ID/?selection=random&amp;picsize=medium&amp;hideself=on&amp;show=collection&amp;n=20&amp;hidelogo=on&amp;cat=drama%7Cmovie%7Cbook%7Cmusic&amp;columns=4"></script>
<h1 style="text-align: center">我想看的电影和书籍<h1>
<script type="text/javascript" src="http://www.douban.com/service/badge/User_ID/?selection=random&amp;picsize=medium&amp;hideself=on&amp;show=wishlist&amp;n=20&amp;hidelogo=on&amp;cat=drama%7Cmovie%7Cbook%7Cmusic&amp;columns=4"></script>
<h1 style="text-align: center">我在看的电影和书籍<h1>
<script type="text/javascript" src="http://www.douban.com/service/badge/User_ID/?selection=random&amp;picsize=medium&amp;hideself=on&amp;show=dolist&amp;n=20&amp;hidelogo=on&amp;cat=drama%7Cmovie%7Cbook%7Cmusic&amp;columns=4"></script>
{% endraw%}

```
