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
<!-- wp:heading -->
<h2>Basic</h2>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>from flask import Flask
app = Flask(__name__)


@app.route('/')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run()</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Integrating MySQL</h2>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>class DataMySQL(Resource):
    def get(self):
        mycursor = mydb.cursor()
        mycursor.execute("select * from data")
        row_headers=[x[0] for x in mycursor.description] #this will extract row headers
        rv = mycursor.fetchall()
        json_data=[]
        for result in rv:
            json_data.append(dict(zip(row_headers,result)))        
        result = json.dumps(json_data, indent=4, sort_keys=True, default=str)
        return jsonify(result)</code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":3} -->
<h3>MySQL Connection</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>mydb = mysql.connector.connect(
  host="localhost",
  user="xxxx",
  passwd="xxxx",
  database="data"
)

mycursor = mydb.cursor()</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Integrating Sqlite</h2>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>class DataSqlite(Resource):
    def get(self):
        conn = db_connect.connect()
        query = conn.execute("select * from data;")
        result = {'data': [dict(zip(tuple (query.keys()) ,i)) for i in query.cursor]}
        return jsonify(result)</code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":3} -->
<h3>SQLite Connection</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>db_connect = create_engine('sqlite:///data.db')</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Connecting to Flask</h2>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>app = Flask(__name__)
api = Api(app)
api.add_resource(DataMySQL, '/datamysql') # Route_MySQL_Data
api.add_resource(DataSqlite, '/datasqlite') # Route_Sqlite_Data</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Initialise</h2>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>from flask import Flask, request, jsonify
from flask_restful import Resource, Api
from sqlalchemy import create_engine
from json import dumps
import mysql.connector
import json
from bson import json_util # pip install pymongo</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Prepare Virtual Environment</h2>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>$ virtualenv venv
$ source venv/bin/activate
$ pip install flask flask-jsonpify flask-sqlalchemy flask-restful pymongo
$ pip freeze
$ sqlite3 data.db</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Run Server</h2>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>$ nohup python server.py &amp; # To Initiate
$ ps ax | grep server.py # To Analyse
$ kill [PID] # To Stop</code></pre>
<!-- /wp:code -->