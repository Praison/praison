---
ID: 427
post_title: Schema Website Markup in JSON-LD
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2015/09/schema-website-markup-in-json-ld/
published: true
post_date: 2015-09-22 10:47:00
---
<pre>&lt;script type="application/ld+json"&gt;
{ "@context": "http://schema.org",
"@type": "WebSite",
"url": "[website url]",
"potentialAction": {
"@type": "SearchAction",
"target": "[website search url]={search_term}",
"query-input": "required name=search_term"
}
}
&lt;/script&gt;</pre>