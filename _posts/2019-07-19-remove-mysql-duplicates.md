---
ID: 1145
post_title: Remove MySQL Duplicates
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2019/07/remove-mysql-duplicates/
published: true
post_date: 2019-07-19 22:33:58
---
<!-- wp:code -->
<pre class="wp-block-code"><code>ALTER IGNORE TABLE `table_name` ADD UNIQUE (title, SID)</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Do not allow duplicates</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>In Settings tab, you can try checking the following values:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Settings -&gt; SQL Queries -&gt; Ignore multiple statement errors</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>If you are using CSV format:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Settings -&gt; Import -&gt; CSV -&gt; Do not abort on INSERT error</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>If you are using SQL format:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Settings -&gt; Export -&gt; SQL -&gt; Use ignore inserts</li></ul>
<!-- /wp:list -->