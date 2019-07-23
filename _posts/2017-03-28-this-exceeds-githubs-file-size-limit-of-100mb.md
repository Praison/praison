---
ID: 737
post_title: 'This exceeds GitHub&#8217;s file size limit of 100MB'
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/03/this-exceeds-githubs-file-size-limit-of-100mb/
published: true
post_date: 2017-03-28 08:55:27
---
Solution for "This exceeds GitHub's file size limit of 100 MB" issue
<pre>git filter-branch -f --index-filter 'git rm --cached --ignore-unmatch YOUR-FILE'</pre>
<pre>git push</pre>