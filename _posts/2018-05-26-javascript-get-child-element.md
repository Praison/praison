---
ID: 967
post_title: JavaScript get child Element
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2018/05/javascript-get-child-element/
published: true
post_date: 2018-05-26 16:59:00
---
<h2>Getting inner Div</h2>
<pre>var mainDiv = document.getElementById('mainDiv'),
childDiv = mainDiv.getElementsByTagName('div')[0],
requiredDiv = childDiv.getElementsByTagName('div')[1];</pre>
&nbsp;