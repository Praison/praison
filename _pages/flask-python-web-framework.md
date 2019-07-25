---
ID: 1167
permalink: /flask-python-web-framework/
post_title: 'Flask: Python web Framework'
author: praison
post_excerpt: ""
layout: page
published: true
post_date: 2019-07-25 14:20:36
---
<!-- wp:code -->
<pre class="wp-block-code"><code>from flask import Flask
app = Flask(__name__)


@app.route('/')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run()</code></pre>
<!-- /wp:code -->