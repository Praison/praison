---
ID: 456
post_title: SEO Canonicalisation
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2015/09/seo-canonicalisation/
published: true
post_date: 2015-09-29 10:07:40
---
<h2>Canonicalisation in terms of SEO</h2>
Show Google which one is the Preferred URL or Main URL
<h2>Canonicalisation Code Implementation</h2>
<pre>&lt;link rel="canonical" href="http://example.com" /&gt;</pre>
<h2>Similar Pages in the eyes of Google</h2>
<strong>All below pages are the same:</strong>
<h3>General</h3>
<ul>
 	<li>http://www.example.com/</li>
 	<li>http://example.com/</li>
</ul>
<h3>Apache Web Server</h3>
<ul>
 	<li>http://example.com/index.html</li>
 	<li>http://www.example.com/index.html</li>
 	<li>http://example.com/index.php</li>
 	<li>http://www.example.com/index.php</li>
</ul>
<h3>Microsoft Internet Information Services (IIS)</h3>
<ul>
 	<li>http://www.example.com/default.asp (or .aspx )</li>
 	<li>http://example.com/default.asp (or .aspx)</li>
</ul>
<h2>Use Redirection to the Preferred URL</h2>
This has to be considered if we have exactly same page with multiple URL's as mentioned above.
<ul>
 	<li>301 HTTP status code : Moved Permanently</li>
 	<li>302 HTTP status code : Moved Temporarily</li>
</ul>
<h2>Canonicalisation for Various Parameters in the URL</h2>
<ul>
 	<li data-wpview-marker="http%3A%2F%2Fwww.example.com%2Fhttp%3A%2Fexample.com%2F">http://example.com/</li>
 	<li data-wpview-marker="http%3A%2F%2Fwww.example.com%2Fhttp%3A%2Fexample.com%2F">http://example.com/?track=123</li>
 	<li data-wpview-marker="http%3A%2F%2Fwww.example.com%2Fhttp%3A%2Fexample.com%2F">http://example.com/?track=431</li>
</ul>
In this above example, the parameter "track" is being used for tracking, in which case the content of the page remains the same.

This has to be explained to Google in order prevent duplicate content issues

Hence canonicalisation is important in terms of On Page SEO