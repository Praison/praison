---
ID: 647
post_title: >
  WP_Query Get Posts Published in the last
  24 hours
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/03/wp_query-get-posts-published-in-the-last-24-hours/
published: true
post_date: 2017-03-06 17:02:44
---
<pre>$args = array(
 'post_type' =&gt; 'post',
 'posts_per_page' =&gt; '10',
 'date_query' =&gt; array(
 array(
 'after' =&gt; '24 hours ago'
 )
 )
 );
$the_posts = new WP_Query( $args );
</pre>