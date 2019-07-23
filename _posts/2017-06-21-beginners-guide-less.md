---
ID: 773
post_title: Beginners Guide to LESS CSS Preprocessor
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/06/beginners-guide-less/
published: true
post_date: 2017-06-21 14:26:53
---
<h2>What is LESS?</h2>
Less is a CSS Preprocessor. http://lesscss.org/
<h2>Installing and Compiling</h2>
<ol>
 	<li>Install Node.js https://nodejs.org/en/</li>
 	<li>using npm ( Node Package Manager ) install LESS globally ( -g )
<ol>
 	<li>
<pre>$ npm install -g less</pre>
</li>
</ol>
</li>
 	<li>
<h3>Compile LESS</h3>
</li>
</ol>
<pre>lessc style.less &gt; style.css</pre>
<ul>
 	<li><em><strong>lessc</strong></em> is used as the command for compiling</li>
</ul>
<h3>Error</h3>
<pre>'lessc' is not recognized as an internal or external command, operable program or batch file.


</pre>
<h3>Solution for this Error</h3>
<strong>Compiling LESS</strong>
<pre>node C:\Folder\Name\node_modules\less\bin\lessc style.less &gt; style.css</pre>
<strong>Note :</strong> <em><strong>\Folder\Name</strong></em> should be the folder in which the <strong>node_modules</strong> have been installed.