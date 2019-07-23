---
ID: 981
post_title: Selenium Firefox Webdriver Python Setup
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2018/07/selenium-firefox-webdriver-python-setup/
published: true
post_date: 2018-07-06 09:44:08
---
<h3>Python Code</h3>
<pre>#Packages

from bs4 import BeautifulSoup
import requests
import pandas as pd
import numpy as np
import csv
import re
from selenium import webdriver


#driver = webdriver.Firefox(capabilities={"marionette":False})
caps = webdriver.DesiredCapabilities.FIREFOX
caps["marionette"] = False
driver = webdriver.Firefox(capabilities=caps)


driver.get("https://www.google.com")

print (driver.title)

</pre>
<h2>Python Code with Headless Firefox</h2>
<h2> </h2>
<pre>#Packages

from bs4 import BeautifulSoup
import requests
import pandas as pd
import numpy as np
import csv
import re
from selenium import webdriver
from selenium.webdriver.firefox.options import Options
options = Options()
options.add_argument("--headless")


#driver = webdriver.Firefox(capabilities={"marionette":False})
caps = webdriver.DesiredCapabilities.FIREFOX
caps["marionette"] = False
driver = webdriver.Firefox(capabilities=caps, firefox_options=options)


driver.get("https://www.google.com")

print (driver.title)

</pre>
<h2>WebDriverException: Message: Can't load the profile</h2>
<p>Try,</p>
<pre>caps["marionette"] = True<br /><br /><br /><br /><br /></pre>
<h2>Get all Divs using Selenium Driver Python</h2>
<p>X Path</p>
<pre>divs = driver.find_elements_by_xpath('//li/div')</pre>
<h3>CSS Selector</h3>
<pre>divs = driver.find_elements_by_css_selector('li &gt; div')</pre>

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->