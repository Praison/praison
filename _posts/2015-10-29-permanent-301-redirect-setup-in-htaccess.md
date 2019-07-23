---
ID: 499
post_title: >
  Permanent 301 Redirect Setup in
  .htaccess
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2015/10/permanent-301-redirect-setup-in-htaccess/
published: true
post_date: 2015-10-29 16:48:55
---
<h2>Redirect old domain to new domain</h2>
<pre>RewriteEngine on
RewriteCond %{HTTP_HOST} ^example.com [NC,OR]
RewriteCond %{HTTP_HOST} ^www.example.com [NC]
RewriteRule ^(.*)$ http://example.<span style="color: #800080;"><b>org</b></span>/$1 [L,R=301,NC]</pre>
<h2>Force Redirect to NON-www version</h2>
<pre>RewriteEngine on
RewriteCond %{HTTP_HOST} ^www.example.com [NC]
RewriteRule ^(.*)$ http://example.com/$1 [L,R=301,NC]</pre>
<h2>Force Redirect to WWW version</h2>
<pre>RewriteEngine on
RewriteCond %{HTTP_HOST} ^example.com [NC]
RewriteRule ^(.*)$ http://www.example.com/$1 [L,R=301,NC]</pre>
<h2>Redirect from HTTPS to HTTP</h2>
<pre>RewriteEngine on
RewriteCond %{HTTPS} on
RewriteRule (.*) http://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]</pre>
<h2>Redirect from HTTP to HTTPS</h2>
<pre>RewriteEngine on
RewriteCond %{HTTPS} off
RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]</pre>
<h2>Redirect files with certain extension</h2>
<pre>RewriteEngine On
RewriteCond %{REQUEST_URI} .aspx$
RewriteRule ^(.*).php$ /$1.php [R=301,L]</pre>
<h2>Redirect Individual Files</h2>
Considering Two Situations
<ol>
 	<li>Redirecting File within the same domain</li>
 	<li>Redirect File to Another Domain</li>
</ol>
<h3>Redirect File with</h3>
<h2>Redirect old domain to new domain</h2>
<pre>RewriteEngine on
RewriteCond %{HTTP_HOST} ^example.com [NC,OR]
RewriteCond %{HTTP_HOST} ^www.example.com [NC]
RewriteRule ^(.*)$ http://example.<span style="color: #800080;"><b>org</b></span>/$1 [L,R=301,NC]</pre>
<h2>Force Redirect to NON-www version</h2>
<pre>RewriteEngine on
RewriteCond %{HTTP_HOST} ^www.example.com [NC]
RewriteRule ^(.*)$ http://example.com/$1 [L,R=301,NC]</pre>
<h2>Force Redirect to WWW version</h2>
<pre>RewriteEngine on
RewriteCond %{HTTP_HOST} ^example.com [NC]
RewriteRule ^(.*)$ http://www.example.com/$1 [L,R=301,NC]</pre>
<h2>Redirect from HTTPS to HTTP</h2>
<pre>RewriteEngine on
RewriteCond %{HTTPS} on
RewriteRule (.*) http://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]</pre>
<h2>Redirect from HTTP to HTTPS</h2>
<pre>RewriteEngine on
RewriteCond %{HTTPS} off
RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]</pre>
<h2>Redirect files with certain extension</h2>
<pre>RewriteEngine On
RewriteCond %{REQUEST_URI} .aspx$
RewriteRule ^(.*).php$ /$1.php [R=301,L]</pre>
<h2>Redirect Individual Files</h2>
Considering Two Situations
<ol>
 	<li>Redirecting File within the same domain</li>
 	<li>Redirect File to Another Domain</li>
</ol>
<h3>Redirect File within the Same Domain</h3>
<pre>Redirect 301 /file1.htm /file2.htm</pre>
<h3>Redirect File to Another Domain</h3>
<pre>Redirect 301 /file1.php http://example.org/file2.php</pre>
in the Same Domain
<pre>Redirect 301 /file1.htm /file2.htm</pre>
<h3>Redirect File to Another Domain</h3>
<pre>Redirect 301 /file1.php http://example.org/file2.php</pre>