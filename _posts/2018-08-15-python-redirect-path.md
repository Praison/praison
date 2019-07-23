---
ID: 996
permalink: /2018/08/python-redirect-path/
post_title: Python Redirect Path
author: praison
post_excerpt: ""
layout: post
published: true
post_date: 2018-08-15 09:05:24
---
<!-- wp:preformatted -->
<pre class="wp-block-preformatted">import requests 
s = requests.Session()
response = s.get("https://google.com/")
cookies = dict(response.cookies)
if response.history:
    print ("Request was redirected")
    for resp in response.history:
        print (resp.status_code, resp.url)
    print ("Final destination:")
    print (response.status_code, response.url)
else:
    print ("Request was not redirected")</pre>
<!-- /wp:preformatted -->