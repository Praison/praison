---
ID: 750
post_title: Ajax Progress Bar
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/04/ajax-progress-bar/
published: true
post_date: 2017-04-05 08:56:07
---
<h2>HTML</h2>
<pre>&lt;style&gt;
 #progress {
 width: 500px;
 border: 1px solid #aaa;
 height: 15px;
 }
 #progress .bar {
 background-color: #bbd;
 height: 15px;
 }
 &lt;/style&gt;
 &lt;div id="progress"&gt;&lt;/div&gt;</pre>
<h2>AJAX</h2>
<pre>&lt;script&gt;

$.ajax({ 

url: ajaxurl.php
success:function(value){
$("#progress").html('&lt;div class="bar" style="width:' + value.percent + '%"&gt;&lt;/div&gt;');
}
}

&lt;/script&gt;</pre>