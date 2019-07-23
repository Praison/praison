---
ID: 962
permalink: /2018/01/is-front-page-is-home/
post_title: 'is_front_page() &#038;&#038; is_home() WordPress Default, Static and Blog Page'
author: praison
post_excerpt: ""
layout: post
published: true
post_date: 2018-01-29 12:08:23
---
<pre>if ( is_front_page() &amp;&amp; is_home() ) {
 // Default homepage

} elseif ( is_front_page()){
 //Static homepage

} elseif ( is_home()){

//Blog page

} else {

//everything else

}</pre>