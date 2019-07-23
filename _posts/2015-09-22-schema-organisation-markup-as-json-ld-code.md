---
ID: 418
permalink: >
  /2015/09/schema-organisation-markup-as-json-ld-code/
post_title: >
  Schema Organisation markup as JSON-LD
  code
author: praison
post_excerpt: ""
layout: post
published: true
post_date: 2015-09-22 10:25:52
---
&nbsp;
<pre>&lt;script type="application/ld+json"&gt;
{ "@context" : "http://schema.org",
"@type" : "Organization",
"name" : "[organization name]",
"logo" : "[logo image url]",
"url" : "[website url]",
"sameAs" : [
"https://twitter.com/[username]",
"https://www.facebook.com/[username]",
"https://www.linkedin.com/company/[username]",
"https://plus.google.com/[username]/posts"
]
}
&lt;/script&gt;</pre>