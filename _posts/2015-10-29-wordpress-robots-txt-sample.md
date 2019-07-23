---
ID: 485
post_title: WordPress Robots.txt Sample
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2015/10/wordpress-robots-txt-sample/
published: true
post_date: 2015-10-29 10:29:40
---
<h2>WordPress Robots.txt</h2>
<pre>User-agent: *
Disallow: /wp-admin/
Disallow: /wp-includes/</pre>
<h2>Adding Sitemaps to WordPress Robots.txt</h2>
<pre>User-agent: *
Disallow: /wp-admin/
Disallow: /wp-includes/

Sitemap: http://www.example.com/post-sitemap.xml</pre>
<h2>Explanation</h2>
<h3>Allowing all Bots</h3>
<ul>
 	<li>Allowing any Bots to Crawl</li>
</ul>
<pre>User-agent: *
Disallow:</pre>
<h3>Not Allowing any Bots</h3>
<ul>
 	<li>Not Allowing any Bots to Crawl</li>
</ul>
<pre>User-agent: *
Disallow: /
</pre>
<h3>Block a Folder</h3>
<pre>User-agent: *
Disallow: /Folder/</pre>
<h3>Block a File</h3>
<pre>User-agent: *
Disallow: /file.html</pre>
<h3> Block a page and/or a directory named private</h3>
<pre>User-agent: *
Disallow: /private</pre>
<h3>Block All Sub Folders starting with private</h3>
<pre>User-agent: *
Disallow: /private*/</pre>
<h3>Block URL's end with</h3>
<pre>User-agent: *
Disallow: /*.asp$</pre>
<h3>Block URL's which includes Question Mark (?)</h3>
<pre>User-agent: *
Disallow: /*?*</pre>
<h3>Block a File Type</h3>
<pre>User-agent: *
Disallow: /*.jpeg$</pre>
<h3>Block all Paginated pages which don't have "?" at the end</h3>
<ul>
 	<li>http://www.example.com/blog/? ( Allow )</li>
 	<li>http://www.example.com/blog/?page=2 ( Not Allow )</li>
</ul>
Helps us to Block Paginated pages from Crawling
<pre>User-agent: *
Disallow: /*? # block URL that includes ?
Allow: /*?$ # allow URL that ends in ?</pre>
<h3>Using Hash</h3>
<pre># Hash is used for commenting out</pre>
<h2>Bots / User Agents</h2>
<h3>Top 10 Bots</h3>
<table style="height: 368px;" width="180">
<tbody>
<tr>
<td width="64">Robot</td>
</tr>
<tr>
<td>bingbot</td>
</tr>
<tr>
<td>Googlebot</td>
</tr>
<tr>
<td>Googlebot Mobile</td>
</tr>
<tr>
<td>AhrefsBot</td>
</tr>
<tr>
<td>Baidu</td>
</tr>
<tr>
<td>MJ12bot</td>
</tr>
<tr>
<td>proximic</td>
</tr>
<tr>
<td>A6</td>
</tr>
<tr>
<td>ADmantX</td>
</tr>
<tr>
<td>msnbot/2.0b</td>
</tr>
</tbody>
</table>
<h3>Individual Crawl request for each Bots</h3>
<pre>User-Agent: Googlebot
Allow: /

User-Agent: Googlebot-Mobile
Allow: /

User-Agent: msnbot
Allow: /

User-Agent: bingbot
Allow: /

# Adsense
User-Agent: Mediapartners-Google
Disallow: / 

# Blekko
User-Agent: ScoutJet
Allow: / 

User-Agent: Yandex
Allow: / 

# CommonCrawl
User-agent: ccbot
Allow: / 

User-agent: baiduspider
Allow: / 

User-agent: DuckDuckBot
Allow: / 

User-Agent: *
Disallow: /</pre>
<h3></h3>