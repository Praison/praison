---
ID: 761
post_title: Beginners Guide to SASS CSS Preprocessor
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/06/beginners-guide-sass/
published: true
post_date: 2017-06-21 13:37:28
---
<h2>What is SASS?</h2>
SASS is a CSS Preprocessor. http://sass-lang.com/
<h2>Installing and compiling</h2>
<ol>
 	<li>Install Ruby <a href="https://rubyinstaller.org/">https://rubyinstaller.org/</a>
<ul>
 	<li>More Info : http://sass-lang.com/install</li>
</ul>
</li>
 	<li>Open Terminal or Command Prompt</li>
</ol>
<pre>gem install sass</pre>
Note : gems is a package manager for Ruby.

3. Check if sass got installed
<pre>sass -v</pre>
4. on a dedicated "test" folder , create two folders "scss" and "css"

C:\test

C:\test\scss

C:\test\css

5. In the <strong>Terminal</strong> or <strong>Command Prompt</strong>

C:\test&gt;
<h2>Compile SASS</h2>
<h3><em><strong>--watch</strong> </em>command</h3>
<em><strong>--watch</strong> </em>command is used to constantly monitor style.scss file for any changes and compile it as soon any change happens.

C:\test&gt; sass --watch scss:css
<pre>sass --watch scss:css</pre>
<h3><em><strong>--watch</strong> </em>dedicated file</h3>
To watch dedicated file style.scss and style.css
<pre>sass --watch style.scss:style.css</pre>
style.scss is the main file

style.css is the complied file
<h2>Minify SASS</h2>
<pre>sass --watch scss:css --style compressed</pre>