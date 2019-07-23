---
ID: 477
post_title: 'Cross Domain Tracking [ Google Analytics ]'
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2015/10/cross-domain-tracking-google-analytics/
published: true
post_date: 2015-10-23 16:04:59
---
Cross Domain Tracking in Google Analytics is for tracking a Visitor across different domains
<h2>Usage</h2>
Tracking the same visitor navigating across
<ol>
 	<li>Various Domain names</li>
 	<li>Various Sub Domains</li>
 	<li>http and https of the same/different domain</li>
 	<li>3rd Party Shopping Carts</li>
 	<li>IFrame</li>
</ol>
<h2>Linking</h2>
( Example )

<strong>Consider two domains :</strong>
<ol>
 	<li>example-1.com : Primary Domain</li>
 	<li>example-2.com : Secondary Domain</li>
</ol>
<h2>Primary Domain</h2>
<pre>&lt;script&gt;

(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){ (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o), m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m) })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

ga('create', 'UA-XXXXXXX-Y', <span class="red-text" style="color: #800080;"><strong>'auto', {'allowLinker': true});
ga('require', 'linker');
ga('linker:autoLink', ['example-2.com'] );</strong></span>
ga('send', 'pageview');

&lt;/script&gt;
</pre>
<h2>Secondary Domain</h2>
<pre>&lt;script&gt;

(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){ (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o), m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m) })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

ga('create', 'UA-XXXXXXX-Y', <span class="red-text" style="color: #800080;"><strong>'auto', {'allowLinker': true});
ga('require', 'linker');
ga('linker:autoLink', ['example-1.com'] );</strong></span>
ga('send', 'pageview');

&lt;/script&gt;</pre>
<h2>Three  or More Domains</h2>
<pre>ga('linker:autoLink', ['example-2.com'<span class="red-text" style="color: #800080;"><strong>, 'example-3.com'</strong></span>] );</pre>
&nbsp;