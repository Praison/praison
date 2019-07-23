---
ID: 1081
post_title: SEO Language Tags
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2018/08/seo-language-tags/
published: true
post_date: 2018-08-29 10:23:14
---
<h2>Language Meta Tag</h2>
<pre>&lt;head&gt;
&lt;meta http-equiv="content-language" content="en-gb" /&gt;
&lt;/head&gt;</pre>
<h2>Language HTTP Response Header</h2>
<h3>Content-Language</h3>
<pre>HTTP/1.1 200 OK
Content-Language: en-gb</pre>
<h3>Link</h3>
<pre>Link: &lt;http://praison.com/file.pdf&gt;; rel="alternate"; hreflang="en",
&lt;http://de-ch.praison.com/file.pdf&gt;; rel="alternate"; hreflang="de-ch",
&lt;http://de.praison.com/file.pdf&gt;; rel="alternate"; hreflang="de"</pre>
<h2>Language &lt;html&gt; Tag Attribute</h2>
<pre>&lt;html lang="en-gb"&gt;
...
&lt;/html&gt;</pre>
<h2>Language Hreflang Tag</h2>
<pre>&lt;link rel="alternate" hreflang="en-gb" href="https://praison.com/en-gb/" /&gt;</pre>
<h2>XML Sitemap Tag</h2>
<pre>&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
xmlns:xhtml="http://www.w3.org/1999/xhtml"&gt;
&lt;url&gt;
&lt;loc&gt;https://prasion.com/english/page.html&lt;/loc&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="de"
href="https://prasion.com/deutsch/page.html"/&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="de-ch"
href="https://prasion.com/schweiz-deutsch/page.html"/&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="en"
href="https://prasion.com/english/page.html"/&gt;
&lt;/url&gt;
&lt;url&gt;
&lt;loc&gt;https://prasion.com/deutsch/page.html&lt;/loc&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="de"
href="https://prasion.com/deutsch/page.html"/&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="de-ch"
href="https://prasion.com/schweiz-deutsch/page.html"/&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="en"
href="https://prasion.com/english/page.html"/&gt;
&lt;/url&gt;
&lt;url&gt;
&lt;loc&gt;https://prasion.com/schweiz-deutsch/page.html&lt;/loc&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="de"
href="https://prasion.com/deutsch/page.html"/&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="de-ch"
href="https://prasion.com/schweiz-deutsch/page.html"/&gt;
&lt;xhtml:link 
rel="alternate"
hreflang="en"
href="https://prasion.com/english/page.html"/&gt;
&lt;/url&gt;
&lt;/urlset&gt;</pre>
&nbsp;